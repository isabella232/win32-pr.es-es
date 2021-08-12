---
description: 'Los siguientes tipos de datos se definen en Volume Shadow Copy API:'
ms.assetid: e64b36d6-4f10-42bd-9ad4-00aba90e9715
title: Tipos de datos de la API de instantáneas de volumen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b159156c4a892ae7ad07a4d988bb8f32b0f5689a440fe3f31da3d6c15470675
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118590567"
---
# <a name="volume-shadow-copy-api-data-types"></a>Tipos de datos de la API de instantáneas de volumen

Los siguientes tipos de datos se definen en Volume Shadow Copy API:

<dl> <dt>

<span id="VSS_ID"></span><span id="vss_id"></span>Identificador \_ de VSS
</dt> <dd>

``` syntax
typedef GUID VSS_ID;
```

La **definición del \_ identificador de VSS** especifica el formato de identificador general de VSS. El **identificador de VSS \_** es un tipo de datos GUID estándar.

**VSS \_ Los** identificadores se usan para identificar lo siguiente: instantáneas, conjuntos de instantáneas, proveedores, versiones de proveedor, escritores (identificador de clase del escritor) e instancias de escritores.

</dd> <dt>

<span id="VSS_PWSZ"></span><span id="vss_pwsz"></span>VSS \_ PWSZ
</dt> <dd>

``` syntax
typedef /* [string][unique] */  __RPC_unique_pointer  __RPC_string WCHAR *VSS_PWSZ;
```

La **definición \_ de PWSZ de VSS** especifica una cadena de caracteres anchos terminada en NULL (wchar).

</dd> <dt>

<span id="VSS_TIMESTAMP"></span><span id="vss_timestamp"></span>MARCA DE TIEMPO DE VSS \_
</dt> <dd>

``` syntax
typedef LONGLONG VSS_TIMESTAMP;
```

La definición TIMESTAMP de **VSS \_** contiene información de marca de tiempo como un valor entero de 64 bits que contiene el número de intervalos de 100 nanosegundos desde el 1 de enero de 1601 (UTC). Esta definición es intercambiable con la [**estructura FILETIME.**](/windows/win32/api/minwinbase/ns-minwinbase-filetime)

</dd> </dl>

 

 
