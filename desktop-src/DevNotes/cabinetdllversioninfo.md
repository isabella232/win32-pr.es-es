---
description: CABINETDLLVERSIONINFO contiene la información de versión de Cabinet.dll.
ms.assetid: 1dc6962c-3087-4f56-8b65-fbf55e17eeb6
title: Estructura CABINETDLLVERSIONINFO
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CABINETDLLVERSIONINFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 9276a03d28bdfeee2b97b44e180bf190cbf20fc40ec58d0aafb44962a6e8fa9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118667988"
---
# <a name="cabinetdllversioninfo-structure"></a>Estructura CABINETDLLVERSIONINFO

\[Esta estructura contiene información necesaria solo cuando se usa **la función DllGetVersion,** que no se admite. Esta documentación solo se proporciona con fines informativos.\]

**CABINETDLLVERSIONINFO contiene** la información de versión de Cabinet.dll.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct {
  DWORD cbStruct;
  DWORD dwReserved1;
  DWORD dwReserved2;
  DWORD dwFileVersionMS;
  DWORD dwFileVersionLS;
} CABINETDLLVERSIONINFO, *PCABINETDLLVERSIONINFO;
```



## <a name="members"></a>Miembros

<dl> <dt>

**cbStruct**
</dt> <dd>

Tamaño de esta estructura, en bytes.

</dd> <dt>

**dwReserved1**
</dt> <dd>

Reservado.

</dd> <dt>

**dwReserved2**
</dt> <dd>

Reservado.

</dd> <dt>

**dwFileVersionMS**
</dt> <dd>

Contiene los bits más significativos de la información de versión. Los bits 0-15 contienen la versión secundaria y los bits 16-31 contienen la versión principal.

</dd> <dt>

**dwFileVersionLS**
</dt> <dd>

Contiene los bits menos significativos de la información de versión. Los bits 0-15 contienen el número de revisión y los bits 16-31 contienen el número de compilación.

</dd> </dl>

## <a name="see-also"></a>Vea también

<dl> <dt>

[**DllGetVersion**](dllgetversion.md)
</dt> </dl>

 

 



