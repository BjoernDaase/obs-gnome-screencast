#
# obs-gnome-screencast. OBS Studio source plugin.
# Copyright (C) 2018 Florian Zwoch <fzwoch@gmail.com>
#
# This file is part of obs-gnome-screencast.
#
# obs-gnome-screencast is free software: you can redistribute it and/or modify
# it under the terms of the GNU General Public License as published by
# the Free Software Foundation, either version 2 of the License, or
# (at your option) any later version.
#
# obs-gnome-screencast is distributed in the hope that it will be useful,
# but WITHOUT ANY WARRANTY; without even the implied warranty of
# MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
# GNU General Public License for more details.
#
# You should have received a copy of the GNU General Public License
# along with obs-gnome-screencast. If not, see <http://www.gnu.org/licenses/>.
#

project('gnome-screencast', 'c',
  meson_version : '>=0.46'
)

link_args = []
if meson.get_compiler('c').has_link_argument('-static-libgcc')
  link_args = '-static-libgcc'
endif

shared_library('gnome-screencast',
  'gnome-screencast.c',
  name_prefix : '',
  dependencies : [
    meson.get_compiler('c').find_library('obs'),
    dependency('gio-2.0'),
    dependency('gstreamer-1.0'),
    dependency('gstreamer-app-1.0'),
    dependency('gdk-3.0')
  ],
  link_args : link_args,
  install : true,
  install_dir : 'lib/obs-plugins'
)
