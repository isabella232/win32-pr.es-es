---
description: Determina si un dispositivo de entrada es compatible con multitoque.
ms.assetid: 4fef7060-2235-4bee-a37b-40d827732b30
title: 'ITablet3:: IsMultiTouch (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet3.IsMultiTouch
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: ed05e110c13af8fe73eebf004183de42eb9fffd7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278476"
---
# <a name="itablet3ismultitouch-method"></a>ITablet3:: IsMultiTouch (método)

Determina si un dispositivo de entrada es compatible con multitoque.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT IsMultiTouch(
  [out] BOOL *bIsMultiTouch
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*bIsMultiTouch* \[ enuncia\]
</dt> <dd>

Indica si el dispositivo es multitoque.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **si \_ es** correcto; de lo contrario, devuelve un código de error como **E \_**.

## <a name="remarks"></a>Observaciones

Después de determinar a través de [**IRealTimeStylus3:: MultiTouchEnabled**](/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus3-get_multitouchenabled) o **ITablet3:: IsMultiTouch** que multitoque está disponible, una aplicación puede optar por participar en los mensajes de entrada de multitoque. Puede encontrar información adicional sobre cómo filtrar métodos multitoque en la sección de propiedades **IRealTimeStylus3:: MultiTouchEnabled** .

## <a name="examples"></a>Ejemplos


```C++
CComQIPtr<ITablet3> spITablet3 = g_spITablet3;
VARIANT_BOOL b;
spITablet3->get_IsMultiTouch(&b);
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                             |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/>                                |
| Biblioteca<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITablet3**](itablet3.md)
</dt> <dt>

[**MultiTouchEnabled**](/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus3-get_multitouchenabled)
</dt> </dl>

 

 




