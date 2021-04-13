---
title: Espacios de nombres
description: Los objetos que residen dentro de un espacio de nombres determinado se identifican mediante un nombre único.
ms.assetid: d42b4b18-d38f-4071-8e3e-9b9b71d46d4b
ms.tgt_platform: multiple
keywords:
- ADSI de espacios de nombres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d29d93963b2fc2b3fa6ea0eb486fe95b46ba0e9e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418351"
---
# <a name="namespaces"></a><span data-ttu-id="63dbc-104">Espacios de nombres</span><span class="sxs-lookup"><span data-stu-id="63dbc-104">Namespaces</span></span>

<span data-ttu-id="63dbc-105">Los objetos que residen dentro de un espacio de nombres determinado se identifican mediante un nombre único.</span><span class="sxs-lookup"><span data-stu-id="63dbc-105">Objects that reside within a given namespace are identified by a unique name.</span></span> <span data-ttu-id="63dbc-106">Por ejemplo, los archivos almacenados en una unidad de disco de PC residen en el espacio de nombres del sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="63dbc-106">For example, files stored on a PC disk drive reside in the file system namespace.</span></span> <span data-ttu-id="63dbc-107">El nombre único de un archivo se basa en la ubicación en la que se almacena en el espacio de nombres del sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="63dbc-107">The unique name of a file is based on where it is stored in the file system namespace.</span></span> <span data-ttu-id="63dbc-108">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="63dbc-108">For example:</span></span>


```C++
C:\public\documents\adsi\adsi_spec.doc
```



<span data-ttu-id="63dbc-109">Los espacios de nombres del servicio de directorio también identifican los objetos que contienen por nombres únicos que normalmente se basan en la ubicación del directorio donde se encuentra el objeto.</span><span class="sxs-lookup"><span data-stu-id="63dbc-109">Directory service namespaces also identify the objects they contain by unique names which are usually based on the location in the directory where the object can be found.</span></span> <span data-ttu-id="63dbc-110">Por ejemplo, en un directorio X. 500, un objeto dado podría tener un nombre similar al siguiente:</span><span class="sxs-lookup"><span data-stu-id="63dbc-110">For example, in an X.500 directory, a given object might have a name like this:</span></span>


```C++
CN=John,OU=Marketing,O=Fabrikam
```



<span data-ttu-id="63dbc-111">Los distintos servicios de directorio usan diferentes formatos para asignar nombres a los objetos que contienen.</span><span class="sxs-lookup"><span data-stu-id="63dbc-111">Different directory services use different forms for naming the objects they contain.</span></span> <span data-ttu-id="63dbc-112">Esto hace que trabajar con distintos espacios de nombres sea desafiante, especialmente para los desarrolladores, considerando todos los distintos entornos en los que se puede estar ejecutando el código.</span><span class="sxs-lookup"><span data-stu-id="63dbc-112">This makes dealing with different namespaces challenging, especially for developers, considering all of the different environments on which the code might be running.</span></span>

<span data-ttu-id="63dbc-113">El objetivo de Active Directory interfaces de servicio (ADSI) es proporcionar un marco de nomenclatura que permita el acceso a los espacios de nombres de diferentes proveedores de servicios de directorio.</span><span class="sxs-lookup"><span data-stu-id="63dbc-113">A goal of Active Directory Service Interfaces (ADSI) is to provide a naming framework that allows access to namespaces of different directory service providers.</span></span>

<span data-ttu-id="63dbc-114">ADSI define una Convención de nomenclatura que puede identificar de forma única un objeto en un entorno heterogéneo.</span><span class="sxs-lookup"><span data-stu-id="63dbc-114">ADSI defines a naming convention that can uniquely identify an object in a heterogeneous environment.</span></span> <span data-ttu-id="63dbc-115">Estos nombres se denominan cadenas ADsPath.</span><span class="sxs-lookup"><span data-stu-id="63dbc-115">These names are called ADsPath strings.</span></span> <span data-ttu-id="63dbc-116">Las cadenas ADsPath tienen varias formas:</span><span class="sxs-lookup"><span data-stu-id="63dbc-116">ADsPath strings take several forms:</span></span>


```C++
"ADs://"
 
"LDAP://"
 
"WinNT://"
```



<span data-ttu-id="63dbc-117">Los diferentes proveedores ADSI pueden introducir formatos ADsPath adicionales (como el proveedor ADSI para el servidor de Internet Information Services, que admiten "IIS://" ADsPaths).</span><span class="sxs-lookup"><span data-stu-id="63dbc-117">Additional ADsPath formats can be introduced by different ADSI providers (such as the ADSI provider for the Internet Information Services server, which support the "IIS://" ADsPaths).</span></span>

 

 




