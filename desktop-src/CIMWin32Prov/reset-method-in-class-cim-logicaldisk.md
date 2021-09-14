---
description: El método Reset de la clase LogicalDisk de CIM \_ solicita un restablecimiento del dispositivo lógico.
ms.assetid: 52c56fbd-c0b5-4621-a08e-58c80481639e
ms.tgt_platform: multiple
title: Método Reset de la CIM_LogicalDisk de datos
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDisk.Reset
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 63eb4c33097be912bffe3031d173956071db774b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126965415"
---
# <a name="reset-method-of-the-cim_logicaldisk-class"></a>Método Reset de la clase \_ LogicalDisk de CIM

El **método Reset** de la clase LogicalDisk de CIM solicita un \_ restablecimiento del dispositivo lógico. Este método se hereda de [**\_ CIM LogicalDevice.**](cim-logicaldevice.md)

> [!IMPORTANT]
> Las clases CIM (Modelo de información común) DE DMTF (Distributed Management Task Force) son las clases primarias en las que se han creado las clases WMI. WMI admite actualmente solo los esquemas [de la versión CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

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

Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF. Microsoft puede haber realizado cambios para corregir errores menores, ajustarse a los estándares de documentación del SDK de Microsoft o proporcionar más información.

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

[Disco \_ lógico CIM](reset-method-in-class-cim-logicaldisk.md)
</dt> <dt>

[**Disco \_ lógico CIM**](cim-logicaldisk.md)
</dt> </dl>

 

 




