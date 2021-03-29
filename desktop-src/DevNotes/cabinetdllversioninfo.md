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
ms.openlocfilehash: b6dfcd68f1bc684554d45feb13b9976465b70efa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907170"
---
# <a name="cabinetdllversioninfo-structure"></a>Estructura CABINETDLLVERSIONINFO

\[Esta estructura contiene información necesaria solo cuando se usa la función **DllGetVersion** , que no se admite. Esta documentación se proporciona solo con fines informativos.\]

**CABINETDLLVERSIONINFO** contiene la información de versión de Cabinet.dll.

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

 

 



