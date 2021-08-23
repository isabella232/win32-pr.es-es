---
description: Establezca la nueva configuración activa del recopilador.
ms.assetid: 1979e657-a8f3-4eab-991c-a884bde10724
ms.tgt_platform: multiple
title: Método SetConfiguration de la clase Control
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.SetConfiguration
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: 41ff2c97eaa4b3e2080493c640b716ae4a822762b0f598c94e141a8cc4b4ac6b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119589075"
---
# <a name="setconfiguration-method-of-the-control-class"></a>Método SetConfiguration de la clase Control

Establezca la nueva configuración activa del recopilador.

## <a name="syntax"></a>Sintaxis


```mof
Uint32 SetConfiguration(
  [in]  string Config,
  [in]  Uint32 OldTimestampLow,
  [in]  Uint32 OldTimestampHigh,
  [out] Uint32 NewTimestampLow,
  [out] Uint32 NewTimestampHigh,
  [out] string ErrorString,
  [out] string WarningString,
  [out] string InfoString,
  [out] uint32 ErrorType
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Configuración* \[ En\]
</dt> <dd>

Configuración que se debe activar.

</dd> <dt>

*OldTimestampLow* \[ En\]
</dt> <dd>

Bits de orden inferior de una marca de tiempo que indica cuándo se estableció la configuración activa actual. La comprobación de atomicidad está habilitada si esta propiedad no está establecida en 0.

</dd> <dt>

*OldTimestampHigh* \[ En\]
</dt> <dd>

Bits de orden superior de una marca de tiempo que indica cuándo se estableció la configuración activa actual. La comprobación de atomicidad está habilitada si esta propiedad no está establecida en 0.

</dd> <dt>

*NewTimestampLow* \[ out\]
</dt> <dd>

Cuando este método devuelve un resultado, este parámetro contiene los bits de orden inferior de una marca de tiempo que indica cuándo se estableció la nueva configuración. La comprobación de atomicidad está habilitada si esta propiedad no está establecida en 0.

</dd> <dt>

*NewTimestampHigh* \[ out\]
</dt> <dd>

Cuando este método devuelve un resultado, este parámetro contiene los bits de orden superior de la marca de tiempo que indica cuándo se estableció la nueva configuración. La comprobación de atomicidad está habilitada si esta propiedad no está establecida en 0.

</dd> <dt>

*ErrorString* \[ out\]
</dt> <dd>

Cuando este método devuelve un resultado, si se produjo un error, este parámetro contiene la descripción del error.

</dd> <dt>

*WarningString* \[ out\]
</dt> <dd>

Cuando este método devuelve un resultado, este parámetro contiene los mensajes de advertencia de la operación.

</dd> <dt>

*InfoString* \[ out\]
</dt> <dd>

Cuando este método devuelve un resultado, este parámetro contiene información para la nueva configuración activa.

</dd> <dt>

*ErrorType* \[ out\]
</dt> <dd>

Cuando este método devuelve un resultado, si se produjo un error, este parámetro indica el tipo de error.

<dt>

0
</dt> <dd>

Falta la nueva configuración.

</dd> <dt>

1
</dt> <dd>

El formato de la nueva configuración no es válido.

</dd> <dt>

2
</dt> <dd>

La nueva configuración no es válida.

</dd> <dt>

3
</dt> <dd>

Se produjo un error debido a un socket abierto.

</dd> <dt>

4
</dt> <dd>

Se produjo un error de escritura de archivo.

</dd> <dt>

5
</dt> <dd>

Se produjo un error de atomicidad.

</dd> </dl> </dd> </dl>

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



| Requisito | Value |
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

 

 




