---
description: Los desarrolladores de bases de datos de instalación deben tener en cuenta dos limitaciones en el control de secuencias mediante la implementación de almacenamiento estructurado OLE de Win32.
ms.assetid: ebd5fcac-0238-4f30-9fd5-a0c5cf9028ef
title: Limitaciones de OLE en secuencias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8ccf2a259b004605381792a4eb9da62d329be91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275758"
---
# <a name="ole-limitations-on-streams"></a><span data-ttu-id="5678a-103">Limitaciones de OLE en secuencias</span><span class="sxs-lookup"><span data-stu-id="5678a-103">OLE Limitations on Streams</span></span>

<span data-ttu-id="5678a-104">Los desarrolladores de bases de datos de instalación deben tener en cuenta dos limitaciones en el control de secuencias mediante la implementación de almacenamiento estructurado OLE de Win32.</span><span class="sxs-lookup"><span data-stu-id="5678a-104">Developers of installation databases need to be aware of two limitations on the handling of streams by the Win32 OLE structured storage implementation.</span></span> <span data-ttu-id="5678a-105">Estas limitaciones pueden afectar a las funciones de instalador de manera indirecta a través de transformaciones y otros datos que se pueden almacenar en la base de datos como una secuencia.</span><span class="sxs-lookup"><span data-stu-id="5678a-105">These limitations can affect installer functions indirectly through transforms and other data that may be stored in the database as a stream.</span></span>

<span data-ttu-id="5678a-106">Hay dos limitaciones relevantes:</span><span class="sxs-lookup"><span data-stu-id="5678a-106">There are two relevant limitations:</span></span>

-   <span data-ttu-id="5678a-107">Los datos binarios se almacenan con un nombre de índice creado mediante la concatenación del nombre de tabla y los valores de las claves principales del registro mediante un delimitador de punto.</span><span class="sxs-lookup"><span data-stu-id="5678a-107">Binary data is stored with an index name created by concatenating the table name and the values of the record's primary keys using a period delimiter.</span></span> <span data-ttu-id="5678a-108">OLE limita los nombres de secuencia a 32 caracteres (31 + terminador nulo).</span><span class="sxs-lookup"><span data-stu-id="5678a-108">OLE limits stream names to 32 characters (31 + null terminator).</span></span> <span data-ttu-id="5678a-109">Windows Installer usa un algoritmo de compresión que puede expandir el límite hasta 62 caracteres en función del carácter.</span><span class="sxs-lookup"><span data-stu-id="5678a-109">Windows Installer uses a compression algorithm that can expand the limit to 62 characters depending upon the character.</span></span> <span data-ttu-id="5678a-110">Tenga en cuenta que el número de caracteres de doble byte es 2.</span><span class="sxs-lookup"><span data-stu-id="5678a-110">Note that double-byte characters count as 2.</span></span>
-   <span data-ttu-id="5678a-111">Aunque puede tener varias secuencias abiertas al mismo tiempo, no puede abrir un flujo por segunda vez hasta que se cierre la primera referencia.</span><span class="sxs-lookup"><span data-stu-id="5678a-111">Although you can have multiple streams open at one time, you cannot open a stream a second time until the first reference is closed.</span></span> <span data-ttu-id="5678a-112">Esto significa que no se puede seleccionar el mismo flujo de datos binarios que se va a abrir en varios registros simultáneamente.</span><span class="sxs-lookup"><span data-stu-id="5678a-112">This means you cannot select the same binary data stream to be open in multiple records simultaneously.</span></span> <span data-ttu-id="5678a-113">Se produce un error al intentar leer los datos binarios del segundo registro.</span><span class="sxs-lookup"><span data-stu-id="5678a-113">Attempts to read the binary data from the second record fail.</span></span> <span data-ttu-id="5678a-114">Tampoco puede cambiar el nombre de las claves principales de un registro mientras haya un flujo de datos binarios en ese registro abierto.</span><span class="sxs-lookup"><span data-stu-id="5678a-114">Also you cannot rename the primary keys of a record while a binary data stream in that record is open.</span></span>

 

 



