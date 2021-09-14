---
description: El método Reset de la clase \_ CIM WORMDrive solicita un restablecimiento del dispositivo lógico.
ms.assetid: ece4a618-6748-45a7-90fe-34eccf0f59d7
ms.tgt_platform: multiple
title: Método reset de la CIM_WORMDrive clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_WORMDrive.Reset
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4fa05b36a1d5cb1d21c4fe53ecebc1fa87bc3991
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126892577"
---
# <a name="reset-method-of-the-cim_wormdrive-class"></a>Método Reset de la clase \_ WORMDrive de CIM

El **método Reset** de la clase CIM \_ [**WORMDrive**](cim-wormdrive.md) solicita un restablecimiento del dispositivo lógico. Este método se hereda de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).

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

Wmi no implementa actualmente este método. Para usar este método, debe implementarlo en su propio proveedor.

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

[CIM \_ WORMDrive](reset-method-in-class-cim-wormdrive.md)
</dt> <dt>

[**CIM \_ WORMDrive**](cim-wormdrive.md)
</dt> </dl>

 

 




