---
title: Control de errores (OpenGL)
description: La función gluErrorString recupera las cadenas de error que corresponden a los códigos de error OpenGL o GLU.
ms.assetid: 59f93c1c-9d15-4980-b246-19257c66b6b8
keywords:
- Utilidad OpenGL (GLU), códigos de error
- GLU (utilidad OpenGL), códigos de error
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab319fd978cd5ea901133fc9961caf1c66f3185d
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104359602"
---
# <a name="handling-errors-opengl"></a>Control de errores (OpenGL)

La función **gluErrorString** recupera las cadenas de error que corresponden a los códigos de error OpenGL o Glu. Los códigos de error de OpenGL definidos actualmente se describen en [**glGetError**](glgeterror.md). Los códigos de error de GLU se enumeran en [**gluErrorString**](gluerrorstring.md), [*gluTessCallback*](glutess.md), [*gluQuadricCallback*](gluquadric.md)y [*gluNurbsCallback*](glunurbs.md).

El valor devuelto para **gluErrorString** es un puntero a una cadena descriptiva que corresponde al número de error OpenGL, Glu o GLX pasado en el parámetro *ErrorCode* . Los códigos de error definidos se describen en el *manual de referencia de OpenGL* junto con la función o función que puede generarlos.

 

 




