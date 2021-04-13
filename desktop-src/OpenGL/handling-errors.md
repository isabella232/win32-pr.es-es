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
# <a name="handling-errors-opengl"></a><span data-ttu-id="334ff-105">Control de errores (OpenGL)</span><span class="sxs-lookup"><span data-stu-id="334ff-105">Handling Errors (OpenGL)</span></span>

<span data-ttu-id="334ff-106">La función **gluErrorString** recupera las cadenas de error que corresponden a los códigos de error OpenGL o Glu.</span><span class="sxs-lookup"><span data-stu-id="334ff-106">The **gluErrorString** function retrieves error strings that correspond to OpenGL or GLU error codes.</span></span> <span data-ttu-id="334ff-107">Los códigos de error de OpenGL definidos actualmente se describen en [**glGetError**](glgeterror.md).</span><span class="sxs-lookup"><span data-stu-id="334ff-107">The currently defined OpenGL error codes are described in [**glGetError**](glgeterror.md).</span></span> <span data-ttu-id="334ff-108">Los códigos de error de GLU se enumeran en [**gluErrorString**](gluerrorstring.md), [*gluTessCallback*](glutess.md), [*gluQuadricCallback*](gluquadric.md)y [*gluNurbsCallback*](glunurbs.md).</span><span class="sxs-lookup"><span data-stu-id="334ff-108">The GLU error codes are listed in [**gluErrorString**](gluerrorstring.md), [*gluTessCallback*](glutess.md), [*gluQuadricCallback*](gluquadric.md), and [*gluNurbsCallback*](glunurbs.md).</span></span>

<span data-ttu-id="334ff-109">El valor devuelto para **gluErrorString** es un puntero a una cadena descriptiva que corresponde al número de error OpenGL, Glu o GLX pasado en el parámetro *ErrorCode* .</span><span class="sxs-lookup"><span data-stu-id="334ff-109">The return value for **gluErrorString** is a pointer to a descriptive string that corresponds to the OpenGL, GLU, or GLX error number passed in the *errorCode* parameter.</span></span> <span data-ttu-id="334ff-110">Los códigos de error definidos se describen en el *manual de referencia de OpenGL* junto con la función o función que puede generarlos.</span><span class="sxs-lookup"><span data-stu-id="334ff-110">The defined error codes are described in the *OpenGL Reference Manual* along with the function or function that can generate them.</span></span>

 

 




