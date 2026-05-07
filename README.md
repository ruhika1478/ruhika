# ruhika
import { Card, CardContent } from "@/components/ui/card";
import { Progress } from "@/components/ui/progress";
import {
  Brain,
  Clock3,
  Flame,
  CheckCircle2,
  Calendar,
  Sparkles,
} from "lucide-react";

export default function NeuroFlowAI() {
  const stats = [
    {
      title: "Focus Time",
      value: "18.4 hrs",
      change: "+12%",
      icon: Clock3,
    },
    {
      title: "Tasks Completed",
      value: "86%",
      change: "+8%",
      icon: CheckCircle2,
    },
    {
      title: "Burnout Risk",
      value: "Low",
      change: "-15%",
      icon: Flame,
    },
    {
      title: "Work Efficiency",
      value: "92%",
      change: "+11%",
      icon: Brain,
    },
  ];

  const recommendations = [
    "Schedule deep work between 9AM–12PM",
    "Reduce meetings on Thursday",
    "Take a 15-minute recharge break",
    "Your productivity spikes after exercise",
  ];

  const tasks = [
    {
      time: "9:00 AM",
      task: "Deep Work Session",
    },
    {
      time: "11:00 AM",
      task: "Marketing Strategy Meeting",
    },
    {
      time: "1:00 PM",
      task: "Analytics Dashboard Review",
    },
    {
      time: "4:00 PM",
      task: "Content Planning",
    },
  ];

  return (
    <div className="min-h-screen bg-[#0b1020] text-white p-8">
      <div className="max-w-7xl mx-auto">
        
        {/* Header */}
        <div className="flex flex-col md:flex-row justify-between items-start md:items-center mb-10">
          <div>
            <h1 className="text-5xl font-black bg-gradient-to-r from-violet-400 to-cyan-400 text-transparent bg-clip-text">
              NeuroFlow AI
            </h1>

            <p className="text-gray-400 mt-2 text-lg">
              AI-powered productivity intelligence platform
            </p>
          </div>

          <button className="mt-5 md:mt-0 px-6 py-3 rounded-2xl bg-gradient-to-r from-violet-500 to-cyan-500 hover:scale-105 transition-all duration-300 shadow-2xl">
            Generate AI Report
          </button>
        </div>

        {/* KPI Cards */}
        <div className="grid grid-cols-1 md:grid-cols-2 xl:grid-cols-4 gap-6 mb-10">
          {stats.map((stat, index) => {
            const Icon = stat.icon;

            return (
              <Card
                key={index}
                className="bg-white/5 border-white/10 backdrop-blur-xl rounded-3xl shadow-2xl"
              >
                <CardContent className="p-6">
                  <div className="flex justify-between items-center">
                    <div>
                      <p className="text-gray-400">{stat.title}</p>

                      <h2 className="text-4xl font-bold mt-3">
                        {stat.value}
                      </h2>

                      <p className="text-green-400 mt-2">
                        {stat.change} this week
                      </p>
                    </div>

                    <div className="w-14 h-14 rounded-2xl bg-gradient-to-br from-violet-500/20 to-cyan-500/20 flex items-center justify-center">
                      <Icon className="text-cyan-300" size={28} />
                    </div>
                  </div>
                </CardContent>
              </Card>
            );
          })}
        </div>

        {/* Main Grid */}
        <div className="grid grid-cols-1 xl:grid-cols-3 gap-6">

          {/* Productivity Section */}
          <div className="xl:col-span-2">
            <Card className="bg-white/5 border-white/10 rounded-3xl backdrop-blur-xl shadow-2xl h-full">
              <CardContent className="p-8">
                <div className="flex justify-between items-center mb-8">
                  <div>
                    <h2 className="text-3xl font-bold">
                      Productivity Insights
                    </h2>

                    <p className="text-gray-400 mt-2">
                      AI-generated behavioral analytics
                    </p>
                  </div>

                  <Sparkles className="text-violet-300" size={34} />
                </div>

                <div className="space-y-8">

                  <div>
                    <div className="flex justify-between mb-2">
                      <p>Focus Score</p>
                      <p>92%</p>
                    </div>

                    <Progress value={92} className="h-4" />
                  </div>

                  <div>
                    <div className="flex justify-between mb-2">
                      <p>Meeting Efficiency</p>
                      <p>74%</p>
                    </div>

                    <Progress value={74} className="h-4" />
                  </div>

                  <div>
                    <div className="flex justify-between mb-2">
                      <p>Burnout Prevention</p>
                      <p>81%</p>
                    </div>

                    <Progress value={81} className="h-4" />
                  </div>

                  <div className="mt-10">
                    <h3 className="text-2xl font-bold mb-5">
                      AI Recommendations
                    </h3>

                    <div className="grid md:grid-cols-2 gap-4">
                      {recommendations.map((item, index) => (
                        <div
                          key={index}
                          className="bg-[#131a2e] border border-white/5 rounded-2xl p-5 hover:scale-[1.02] transition-all"
                        >
                          <p className="text-gray-300">{item}</p>
                        </div>
                      ))}
                    </div>
                  </div>
                </div>
              </CardContent>
            </Card>
          </div>

          {/* Schedule Panel */}
          <div>
            <Card className="bg-white/5 border-white/10 rounded-3xl backdrop-blur-xl shadow-2xl h-full">
              <CardContent className="p-8">
                <div className="flex items-center justify-between mb-8">
                  <div>
                    <h2 className="text-3xl font-bold">
                      Smart Schedule
                    </h2>

                    <p className="text-gray-400 mt-2">
                      Optimized by AI
                    </p>
                  </div>

                  <Calendar className="text-cyan-300" size={30} />
                </div>

                <div className="space-y-5">
                  {tasks.map((task, index) => (
                    <div
                      key={index}
                      className="bg-[#131a2e] rounded-2xl p-5 border border-white/5"
                    >
                      <p className="text-cyan-300 font-semibold">
                        {task.time}
                      </p>

                      <h3 className="text-lg font-medium mt-2">
                        {task.task}
                      </h3>
                    </div>
                  ))}
                </div>

                <div className="mt-10 p-6 rounded-3xl bg-gradient-to-br from-violet-500/20 to-cyan-500/20 border border-violet-400/20">
                  <p className="text-sm uppercase tracking-widest text-gray-300">
                    AI Insight
                  </p>

                  <h3 className="text-2xl font-bold mt-3 leading-snug">
                    Your highest productivity window is between
                    9AM–12PM.
                  </h3>
                </div>
              </CardContent>
            </Card>
          </div>
        </div>
      </div>
    </div>
  );
}
