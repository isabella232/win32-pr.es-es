---
description: 'Los siguientes tipos de datos se definen en la API de instantáneas de volumen:'
ms.assetid: e64b36d6-4f10-42bd-9ad4-00aba90e9715
title: Tipos de datos de la API de instantáneas de volumen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99717bc87a59ee03cb93ef7f6abbdf429e3d3bec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809836"
---
# <a name="volume-shadow-copy-api-data-types"></a><span data-ttu-id="489fe-103">Tipos de datos de la API de instantáneas de volumen</span><span class="sxs-lookup"><span data-stu-id="489fe-103">Volume Shadow Copy API Data Types</span></span>

<span data-ttu-id="489fe-104">Los siguientes tipos de datos se definen en la API de instantáneas de volumen:</span><span class="sxs-lookup"><span data-stu-id="489fe-104">The following data types are defined in the Volume Shadow Copy API:</span></span>

<dl> <dt>

<span data-ttu-id="489fe-105"><span id="VSS_ID"></span><span id="vss_id"></span>identificador de VSS \_</span><span class="sxs-lookup"><span data-stu-id="489fe-105"><span id="VSS_ID"></span><span id="vss_id"></span>VSS\_ID</span></span>
</dt> <dd>

``` syntax
typedef GUID VSS_ID;
```

<span data-ttu-id="489fe-106">La definición de **\_ identificador de VSS** especifica el formato de identificador de VSS general.</span><span class="sxs-lookup"><span data-stu-id="489fe-106">The **VSS\_ID** definition specifies the general VSS identifier format.</span></span> <span data-ttu-id="489fe-107">El **\_ identificador de VSS** es un tipo de datos de GUID estándar.</span><span class="sxs-lookup"><span data-stu-id="489fe-107">The **VSS\_ID** is a standard GUID data type.</span></span>

<span data-ttu-id="489fe-108">**VSS \_ Los IDENTIFICADOres** se usan para identificar lo siguiente: instantáneas, conjuntos de instantáneas, proveedores, versiones de proveedor, escritores (identificador de clase del escritor) e instancias de escritores.</span><span class="sxs-lookup"><span data-stu-id="489fe-108">**VSS\_ID** s are used to identify the following: shadow copies, shadow copy sets, providers, provider versions, writers (writer's class identifier), and instances of writers.</span></span>

</dd> <dt>

<span data-ttu-id="489fe-109"><span id="VSS_PWSZ"></span><span id="vss_pwsz"></span>PWSZ de VSS \_</span><span class="sxs-lookup"><span data-stu-id="489fe-109"><span id="VSS_PWSZ"></span><span id="vss_pwsz"></span>VSS\_PWSZ</span></span>
</dt> <dd>

``` syntax
typedef /* [string][unique] */  __RPC_unique_pointer  __RPC_string WCHAR *VSS_PWSZ;
```

<span data-ttu-id="489fe-110">La **definición \_ PWSZ de VSS** especifica una cadena de caracteres anchos terminada en null (WCHAR).</span><span class="sxs-lookup"><span data-stu-id="489fe-110">The **VSS\_PWSZ** definition specifies a null-terminated wide character string (wchar).</span></span>

</dd> <dt>

<span data-ttu-id="489fe-111"><span id="VSS_TIMESTAMP"></span><span id="vss_timestamp"></span>marca de tiempo de VSS \_</span><span class="sxs-lookup"><span data-stu-id="489fe-111"><span id="VSS_TIMESTAMP"></span><span id="vss_timestamp"></span>VSS\_TIMESTAMP</span></span>
</dt> <dd>

``` syntax
typedef LONGLONG VSS_TIMESTAMP;
```

<span data-ttu-id="489fe-112">La definición de la **\_ marca** de tiempo de VSS contiene información de marca de tiempo como un valor entero de 64 bits que contiene el número de intervalos de 100-nanosegundos desde el 1 de enero de 1601 (UTC).</span><span class="sxs-lookup"><span data-stu-id="489fe-112">The **VSS\_TIMESTAMP** definition holds time-stamp information as a 64-bit integer value containing the number of 100-nanosecond intervals since January 1, 1601 (UTC).</span></span> <span data-ttu-id="489fe-113">Esta definición es intercambiable con la estructura [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) .</span><span class="sxs-lookup"><span data-stu-id="489fe-113">This definition is interchangeable with the [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) structure.</span></span>

</dd> </dl>

 

 
