---
description: Validar un texto de configuración para comprobar su exactitud sin establecerlo activo. Devuelve 1 si se realiza correctamente, 0 en caso de error.
ms.assetid: baeabed0-7717-498a-9886-e49e4a101711
ms.tgt_platform: multiple
title: Método ValidateConfiguration de la clase control
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.ValidateConfiguration
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: d4e1d0061b779a54973aeea1a487d8838781cf6c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998081"
---
# <a name="validateconfiguration-method-of-the-control-class"></a>Método ValidateConfiguration de la clase control

Validar un texto de configuración para comprobar su exactitud sin establecerlo activo. Devuelve 1 si se realiza correctamente, 0 en caso de error.

## <a name="syntax"></a>Sintaxis


```mof
Uint32 ValidateConfiguration(
  [in]  string Config,
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

Configuración que se va a comprobar.

</dd> <dt>

*ErrorString* \[ enuncia\]
</dt> <dd>

Cuando este método devuelve un error, este parámetro contiene una descripción del error de validación de la operación.

</dd> <dt>

*WarningString* \[ enuncia\]
</dt> <dd>

Cuando este método finaliza, este parámetro contiene una descripción de las advertencias de validación para la operación.

Cadena de texto con advertencias.

</dd> <dt>

*InfoString* \[ enuncia\]
</dt> <dd>

Cuando este método finaliza, este parámetro contiene un conjunto de información sobre la configuración.

</dd> <dt>

*ErrorType* \[ enuncia\]
</dt> <dd>

Cuando este método finaliza, si se produjo un error de validación, este parámetro indica el tipo de error.

Los valores posibles son:

<dt>

0
</dt> <dd>

Falta el argumento.

</dd> <dt>

1
</dt> <dd>

El formato del argumento no es válido.

</dd> <dt>

2
</dt> <dd>

Un argumento de configuración no es válido.

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

 

 




