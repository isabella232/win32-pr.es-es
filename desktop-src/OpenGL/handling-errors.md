---
title: Control de errores (OpenGL)
description: La función gluErrorString recupera cadenas de error que corresponden a códigos de error OpenGL o GLU.
ms.assetid: 59f93c1c-9d15-4980-b246-19257c66b6b8
keywords:
- Utilidad OpenGL (GLU),códigos de error
- GLU (utilidad OpenGL),códigos de error
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75ac3fd9010862dd9c567cb7688f7f96286cae06f7e3b0e4ffe73d3b41ca9b67
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120035195"
---
# <a name="handling-errors-opengl"></a>Control de errores (OpenGL)

La **función gluErrorString** recupera cadenas de error que corresponden a códigos de error OpenGL o GLU. Los códigos de error de OpenGL definidos actualmente se describen [**en glGetError**](glgeterror.md). Los códigos de error de GLU se enumeran [**en gluErrorString**](gluerrorstring.md), [*gluTessCallback*](glutess.md), [*gluQuadricCallback*](gluquadric.md)y [*gluNurbsCallback*](glunurbs.md).

El valor devuelto para **gluErrorString** es un puntero a una cadena descriptiva que corresponde al número de error de OpenGL, GLU o GLX pasado en el *parámetro errorCode.* Los códigos de error definidos se describen en el Manual de *referencia de OpenGL* junto con la función o función que puede generarlos.

 

 




