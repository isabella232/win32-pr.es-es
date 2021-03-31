---
title: Longitudes de búfer de funciones de administración de red
description: En este tema se describen los requisitos para las longitudes de búfer de función cuando se usan con las API de administración de redes.
ms.assetid: 08599966-68a1-420b-bbc7-6daac833d08f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5003f739d235a099adb9f4f403c15c67bd9169e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903518"
---
# <a name="network-management-function-buffer-lengths"></a><span data-ttu-id="0e0cf-103">Longitudes de búfer de funciones de administración de red</span><span class="sxs-lookup"><span data-stu-id="0e0cf-103">Network Management Function Buffer Lengths</span></span>

<span data-ttu-id="0e0cf-104">En este tema se describen los requisitos para las longitudes de búfer de función cuando se usan con las API de administración de redes.</span><span class="sxs-lookup"><span data-stu-id="0e0cf-104">This topic discusses the requirements for function buffer lengths when used with the network management APIs.</span></span>

<span data-ttu-id="0e0cf-105">Las aplicaciones que especifican tamaños de búfer al llamar a las funciones de enumeración de administración de redes (y a varias funciones de recuperación de datos) deben especificar los búferes lo suficientemente grandes como para contener la estructura (o estructuras) de información devuelta más las cadenas a las que apuntan sus miembros.</span><span class="sxs-lookup"><span data-stu-id="0e0cf-105">Applications that specify buffer sizes when calling network management enumeration functions (and various data retrieval functions) must specify buffers large enough to hold the returned information structure (or structures) plus the strings to which their members point.</span></span> <span data-ttu-id="0e0cf-106">Si no especifica un búfer suficientemente grande para recibir todas las entradas disponibles, la función devuelve los datos de \_ error \_ .</span><span class="sxs-lookup"><span data-stu-id="0e0cf-106">If you do not specify a large enough buffer to receive all the available entries, the function returns ERROR\_MORE\_DATA.</span></span> <span data-ttu-id="0e0cf-107">Las llamadas de enumeración no devuelven entradas parciales.</span><span class="sxs-lookup"><span data-stu-id="0e0cf-107">Enumeration calls do not return partial entries.</span></span>

<span data-ttu-id="0e0cf-108">Algunas funciones de administración de red toman un parámetro de longitud máxima de datos de consulta, *prefmaxlen*.</span><span class="sxs-lookup"><span data-stu-id="0e0cf-108">Some network management functions take an advisory maximum data-length parameter, *prefmaxlen*.</span></span> <span data-ttu-id="0e0cf-109">Este parámetro permite a una aplicación sugerir el número de bytes que el servidor debe devolver desde una llamada de función.</span><span class="sxs-lookup"><span data-stu-id="0e0cf-109">This parameter allows an application to suggest the number of bytes the server should return from a function call.</span></span>

<span data-ttu-id="0e0cf-110">Si especifica el valor \_ de longitud máxima preferida \_ en el parámetro *prefmaxlen* , las funciones de administración de red asignarán la cantidad de memoria necesaria para los datos.</span><span class="sxs-lookup"><span data-stu-id="0e0cf-110">If you specify the value MAX\_PREFERRED\_LENGTH in the *prefmaxlen* parameter, the network management functions allocate the amount of memory required for the data.</span></span>

<span data-ttu-id="0e0cf-111">Para obtener más información, consulte [búferes de funciones de administración de red](network-management-function-buffers.md).</span><span class="sxs-lookup"><span data-stu-id="0e0cf-111">For more information, see [Network Management Function Buffers](network-management-function-buffers.md).</span></span>

 

 




