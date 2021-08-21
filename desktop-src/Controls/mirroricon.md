---
title: Función MirrorIcon
description: Invierte los iconos (reflejos) para que se muestren correctamente en un contexto de dispositivo reflejado.
ms.assetid: bca87037-1789-466b-9be0-914966fdad31
keywords:
- Controles de función MirrorIcon Windows
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
ms.openlocfilehash: e597c344b5499272778ced3ff4cc2269fd7685ba6f554568c8493a6f65826bdd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119078949"
---
# <a name="mirroricon-function"></a>Función MirrorIcon

\[**MirrorIcon** está disponible a través Windows XP con Service Pack 2 (SP2). Podría modificarse o no estar disponible en versiones posteriores.\]

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

*phIconSmall* \[ in, out, optional\]
</dt> <dd>

Tipo: **[ **HICON**](/windows/desktop/WinProg/windows-data-types)\***

Puntero al identificador de icono que hace referencia a una versión pequeña de un icono.

</dd> <dt>

*phIconLarge* \[ in, out, optional\]
</dt> <dd>

Tipo: **[ **HICON**](/windows/desktop/WinProg/windows-data-types)\***

Puntero al identificador de icono que hace referencia a una versión grande de un icono.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **BOOL**](/windows/desktop/WinProg/windows-data-types)**

**TRUE** si se realiza correctamente; de lo contrario, **FALSE**.

## <a name="remarks"></a>Comentarios

**MirrorIcon** no se exporta por nombre ni se declara en un archivo de encabezado público. Para usarlo, debe usar [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) y solicitar ordinal 414 a ComCtl32.dll para obtener un puntero de función.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                                  |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                            |
| Archivo DLL<br/>                      | <dl> <dt>Comctl32.dll (versión 5.81 o posterior)</dt> </dl> |



 

