---
title: Control de errores (OpenGL)
description: La función gluErrorString recupera cadenas de error que corresponden a códigos de error OpenGL o GLU.
ms.assetid: 59f93c1c-9d15-4980-b246-19257c66b6b8
keywords:
- Utilidad OpenGL (GLU),códigos de error
- GLU (utilidad OpenGL),códigos de error
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab319fd978cd5ea901133fc9961caf1c66f3185d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476675"
---
# <a name="handling-errors-opengl"></a>Control de errores (OpenGL)

La **función gluErrorString** recupera cadenas de error que corresponden a códigos de error OpenGL o GLU. Los códigos de error de OpenGL definidos actualmente se describen [**en glGetError**](glgeterror.md). Los códigos de error de GLU se enumeran [**en gluErrorString**](gluerrorstring.md), [*gluTessCallback*](glutess.md), [*gluQuadricCallback*](gluquadric.md)y [*gluNurbsCallback*](glunurbs.md).

El valor devuelto para **gluErrorString** es un puntero a una cadena descriptiva que corresponde al número de error de OpenGL, GLU o GLX pasado en el *parámetro errorCode.* Los códigos de error definidos se describen en el Manual de *referencia de OpenGL* junto con la función o función que puede generarlos.

 

 




