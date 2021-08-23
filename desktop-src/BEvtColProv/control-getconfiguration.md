---
description: Lea la configuración activa del recopilador.
ms.assetid: ea26142d-5dcd-466d-b9df-5349f58a190f
ms.tgt_platform: multiple
title: Método GetConfiguration de la clase Control
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.GetConfiguration
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: a877b4ae061b6568b877d9b8ee65b8d9b0380a012d7fdba28408ad4bfcae7030
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119579725"
---
# <a name="getconfiguration-method-of-the-control-class"></a>Método GetConfiguration de la clase Control

Lea la configuración activa del recopilador.

## <a name="syntax"></a>Sintaxis


```mof
Uint32 GetConfiguration(
  [out] Uint32 TimestampLow,
  [out] Uint32 TimestampHigh
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*TimestampLow* \[ out\]
</dt> <dd>

Cuando este método devuelve un resultado, este parámetro contiene los bits de orden inferior de una marca de tiempo que indica cuándo se estableció la configuración.

</dd> <dt>

*TimestampHigh* \[ out\]
</dt> <dd>

Cuando este método devuelve un resultado, este parámetro contiene los bits de orden superior de una marca de tiempo que indica cuándo se estableció la configuración.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

<dl> <dt>


</dt> <dd>

0

Error

</dd> <dt>


</dt> <dd>

1

Correcto

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 10 solo aplicaciones de escritorio\]<br/>                                                          |
| Servidor mínimo compatible<br/> | Windows Server 2016<br/>                                                                       |
| Espacio de nombres<br/>                | Raíz \\ de Microsoft Windows \\ \\ BootEventCollector<br/>                                              |
| MOF<br/>                      | <dl> <dt>BootEventCollectorWMI.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>BEvtCol.exe</dt> </dl>               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Control**](control.md)
</dt> </dl>

 

 




