---
title: ADsPath de Winnt
description: En este tema se incluyen ejemplos de cadenas que se usan para el ADsPath de Winnt.
ms.assetid: 0fad4b34-5287-43a0-a172-a08955b8b132
ms.tgt_platform: multiple
keywords:
- Proveedor de servicios de WinNT ADSI, ADsPath de Winnt
- ADsPath ADSI, WinNT, descripción
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 906ea2c3db1b5234fb07045d921858766a105c4c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103993830"
---
# <a name="winnt-adspath"></a><span data-ttu-id="d3bca-105">ADsPath de Winnt</span><span class="sxs-lookup"><span data-stu-id="d3bca-105">WinNT ADsPath</span></span>

<span data-ttu-id="d3bca-106">La cadena ADsPath del proveedor WinNT de ADSI puede ser una de las siguientes formas:</span><span class="sxs-lookup"><span data-stu-id="d3bca-106">The ADsPath string for the ADSI WinNT provider can be one of the following forms:</span></span>


```C++
WinNT:
WinNT://<domain name>
WinNT://<domain name>/<server>
WinNT://<domain name>/<path>
WinNT://<domain name>/<object name>
WinNT://<domain name>/<object name>,<object class>
WinNT://<server>
WinNT://<server>/<object name>
WinNT://<server>/<object name>,<object class>
```



<span data-ttu-id="d3bca-107">El nombre de dominio puede ser un nombre NETBIOS o un nombre DNS.</span><span class="sxs-lookup"><span data-stu-id="d3bca-107">The domain name can be either a NETBIOS name or a DNS name.</span></span>

<span data-ttu-id="d3bca-108">El servidor es el nombre de un servidor específico dentro del dominio.</span><span class="sxs-lookup"><span data-stu-id="d3bca-108">The server is the name of a specific server within the domain.</span></span>

<span data-ttu-id="d3bca-109">La ruta de acceso es la ruta de acceso de en el objeto, como "servidorimpresión1/Printer2".</span><span class="sxs-lookup"><span data-stu-id="d3bca-109">The path is the path of on object, such as "printserver1/printer2".</span></span>

<span data-ttu-id="d3bca-110">El nombre del objeto es el nombre de un objeto específico.</span><span class="sxs-lookup"><span data-stu-id="d3bca-110">The object name is the name of a specific object.</span></span>

<span data-ttu-id="d3bca-111">La clase de objeto es el nombre de clase del objeto con nombre.</span><span class="sxs-lookup"><span data-stu-id="d3bca-111">The object class is the class name of the named object.</span></span> <span data-ttu-id="d3bca-112">Un ejemplo de este uso sería "WinNT://MyServer/JeffSmith,user".</span><span class="sxs-lookup"><span data-stu-id="d3bca-112">One example of this usage would be "WinNT://MyServer/JeffSmith,user".</span></span> <span data-ttu-id="d3bca-113">Especificar un nombre de clase puede mejorar el rendimiento de la operación de enlace.</span><span class="sxs-lookup"><span data-stu-id="d3bca-113">Specifying a class name can improve the performance of the bind operation.</span></span>

 

 




