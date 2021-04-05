---
title: MirrorIcon función)
description: Invierte los iconos (reflejos) para que se muestren correctamente en un contexto de dispositivo reflejado.
ms.assetid: bca87037-1789-466b-9be0-914966fdad31
keywords:
- MirrorIcon (función) controles de Windows
topic_type:
- apiref
api_name:
- MirrorIcon
api_location:
- Comctl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02f180d509464b63e5ec73c5fb74e4d70386bdea
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079001"
---
# <a name="mirroricon-function"></a>MirrorIcon función)

\[**MirrorIcon** está disponible a través de Windows XP con Service Pack 2 (SP2). Podría modificarse o no estar disponible en versiones posteriores.\]

Invierte los iconos (reflejos) para que se muestren correctamente en un contexto de dispositivo reflejado.

## <a name="syntax"></a>Sintaxis


```C++
BOOL WINAPI MirrorIcon(
  _Inout_opt_ HICON *phIconSmall,
  _Inout_opt_ HICON *phIconLarge
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*phIconSmall* \[ in, out, opcional\]
</dt> <dd>

Tipo: **[**HICON**](/windows/desktop/WinProg/windows-data-types) \** _

Puntero al identificador de icono que hace referencia a una versión pequeña de un icono.

</dd> <dt>

_phIconLarge * \[ in, out, Optional\]
</dt> <dd>

Tipo: **[**HICON**](/windows/desktop/WinProg/windows-data-types) \** _

Puntero al identificador de icono que hace referencia a una versión grande de un icono.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: _ *[**bool**](/windows/desktop/WinProg/windows-data-types)**

**True si es** correcto; en caso contrario, **false**.

## <a name="remarks"></a>Observaciones

**MirrorIcon** no se exporta por nombre o se declara en un archivo de encabezado público. Para usarlo, debe utilizar [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) y el ordinal de solicitud 414 de ComCtl32.dll para obtener un puntero de función.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                                  |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                            |
| Archivo DLL<br/>                      | <dl> <dt>Comctl32.dll (versión 5,81 o posterior)</dt> </dl> |



 

