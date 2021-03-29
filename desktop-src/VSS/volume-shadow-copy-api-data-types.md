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
# <a name="volume-shadow-copy-api-data-types"></a>Tipos de datos de la API de instantáneas de volumen

Los siguientes tipos de datos se definen en la API de instantáneas de volumen:

<dl> <dt>

<span id="VSS_ID"></span><span id="vss_id"></span>identificador de VSS \_
</dt> <dd>

``` syntax
typedef GUID VSS_ID;
```

La definición de **\_ identificador de VSS** especifica el formato de identificador de VSS general. El **\_ identificador de VSS** es un tipo de datos de GUID estándar.

**VSS \_ Los IDENTIFICADOres** se usan para identificar lo siguiente: instantáneas, conjuntos de instantáneas, proveedores, versiones de proveedor, escritores (identificador de clase del escritor) e instancias de escritores.

</dd> <dt>

<span id="VSS_PWSZ"></span><span id="vss_pwsz"></span>PWSZ de VSS \_
</dt> <dd>

``` syntax
typedef /* [string][unique] */  __RPC_unique_pointer  __RPC_string WCHAR *VSS_PWSZ;
```

La **definición \_ PWSZ de VSS** especifica una cadena de caracteres anchos terminada en null (WCHAR).

</dd> <dt>

<span id="VSS_TIMESTAMP"></span><span id="vss_timestamp"></span>marca de tiempo de VSS \_
</dt> <dd>

``` syntax
typedef LONGLONG VSS_TIMESTAMP;
```

La definición de la **\_ marca** de tiempo de VSS contiene información de marca de tiempo como un valor entero de 64 bits que contiene el número de intervalos de 100-nanosegundos desde el 1 de enero de 1601 (UTC). Esta definición es intercambiable con la estructura [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) .

</dd> </dl>

 

 
