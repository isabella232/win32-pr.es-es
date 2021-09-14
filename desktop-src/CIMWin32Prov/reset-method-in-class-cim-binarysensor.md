---
description: El método Reset de la clase BinarySensor de CIM \_ solicita un restablecimiento del dispositivo lógico.
ms.assetid: 73ae915d-9649-4eca-8f9b-fb4165c94cbe
ms.tgt_platform: multiple
title: Método Reset de la CIM_BinarySensor clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BinarySensor.Reset
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0f636cf277e144dc827adc0891d41dc136ce0a99
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062635"
---
# <a name="reset-method-of-the-cim_binarysensor-class"></a>Método Reset de la clase \_ BinarySensor de CIM

El **método Reset** de la clase BinarySensor de CIM solicita un \_ restablecimiento del dispositivo lógico. Este método se hereda de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).

> [!IMPORTANT]
> Las clases CIM (Modelo de información común) DMTF (Distributed Management Task Force) son las clases primarias en las que se han creado las clases WMI. WMI admite actualmente solo los esquemas [de versión CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

## <a name="syntax"></a>Sintaxis


```mof
uint32 Reset();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve 0 (cero) si la solicitud se ejecutó correctamente, 1 (uno) si no se admite la solicitud y algún otro valor si se produjo un error.

## <a name="remarks"></a>Observaciones

Actualmente, WMI no implementa este método. Para usar este método, debe implementarlo en su propio proveedor.

Esta documentación se deriva de las descripciones de clases CIM publicadas por dmtf. Microsoft puede haber realizado cambios para corregir errores menores, ajustarse a los estándares de documentación del SDK de Microsoft o proporcionar más información.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[CIM \_ BinarySensor](reset-method-in-class-cim-binarysensor.md)
</dt> <dt>

[**CIM \_ BinarySensor**](cim-binarysensor.md)
</dt> </dl>

 

 




