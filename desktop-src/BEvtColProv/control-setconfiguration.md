---
description: Establezca la nueva configuración activa del recopilador.
ms.assetid: 1979e657-a8f3-4eab-991c-a884bde10724
ms.tgt_platform: multiple
title: Método SetConfiguration de la clase control
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
ms.openlocfilehash: 4f482de9c4cd8f410371da51e605762a1f92e104
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103806986"
---
# <a name="setconfiguration-method-of-the-control-class"></a>Método SetConfiguration de la clase control

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

*Configuración* \[ de de\]
</dt> <dd>

Configuración que se va a activar.

</dd> <dt>

*OldTimestampLow* \[ de\]
</dt> <dd>

Bits de orden inferior de una marca de tiempo que indica cuándo se estableció la configuración activa actual. La comprobación de atomicidad está habilitada si esta propiedad no está establecida en 0.

</dd> <dt>

*OldTimestampHigh* \[ de\]
</dt> <dd>

Bits de orden superior de una marca de tiempo que indica cuándo se estableció la configuración activa actual. La comprobación de atomicidad está habilitada si esta propiedad no está establecida en 0.

</dd> <dt>

*NewTimestampLow* \[ enuncia\]
</dt> <dd>

Cuando este método finaliza, este parámetro contiene los bits de orden inferior de una marca de tiempo que indica cuándo se estableció la nueva configuración. La comprobación de atomicidad está habilitada si esta propiedad no está establecida en 0.

</dd> <dt>

*NewTimestampHigh* \[ enuncia\]
</dt> <dd>

Cuando este método finaliza, este parámetro contiene los bits de orden superior de la marca de tiempo que indica cuándo se estableció la nueva configuración. La comprobación de atomicidad está habilitada si esta propiedad no está establecida en 0.

</dd> <dt>

*ErrorString* \[ enuncia\]
</dt> <dd>

Cuando este método devuelve un error, este parámetro contiene la descripción del error.

</dd> <dt>

*WarningString* \[ enuncia\]
</dt> <dd>

Cuando este método finaliza, este parámetro contiene cualquier mensaje de advertencia para la operación.

</dd> <dt>

*InfoString* \[ enuncia\]
</dt> <dd>

Cuando este método finaliza, este parámetro contiene información para la nueva configuración activa.

</dd> <dt>

*ErrorType* \[ enuncia\]
</dt> <dd>

Cuando este método devuelve un error, este parámetro indica el tipo de error.

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

Error producido por un socket abierto.

</dd> <dt>

4
</dt> <dd>

Se produjo un error de escritura en el archivo.

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
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10 \[\]<br/>                                                          |
| Servidor mínimo compatible<br/> | Windows Server 2016<br/>                                                                       |
| Espacio de nombres<br/>                | Raíz de \\ Microsoft \\ Windows \\ BootEventCollector<br/>                                              |
| MOF<br/>                      | <dl> <dt>BootEventCollectorWMI. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>BEvtCol.exe</dt> </dl>               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Control**](control.md)
</dt> </dl>

 

 




