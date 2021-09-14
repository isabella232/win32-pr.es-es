---
description: El método Reset de la clase \_ CIM PCVideoController solicita un restablecimiento del dispositivo lógico.
ms.assetid: 0dbed7af-6c7a-4bbb-b1ae-d768d2f88697
ms.tgt_platform: multiple
title: Método Reset de la CIM_PCVideoController clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PCVideoController.Reset
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: b156f4c440e98ebc51618ca8350696f23b55074b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126965375"
---
# <a name="reset-method-of-the-cim_pcvideocontroller-class"></a>Método Reset de la \_ clase PCVideoController de CIM

El **método Reset** de la clase CIM \_ PCVideoController solicita un restablecimiento del dispositivo lógico. Este método se hereda de [**\_ CIM LogicalDevice.**](cim-logicaldevice.md)

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

Wmi no implementa actualmente este método. Para usar este método, debe implementarlo en su propio proveedor. Para las clases WMI derivadas de [**\_ CIM PCVideoController,**](cim-pcvideocontroller.md)vea [Clases Win32](win32-provider.md).

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

[CIM \_ PCVideoController](reset-method-in-class-cim-pcvideocontroller.md)
</dt> <dt>

[**CIM \_ PCVideoController**](cim-pcvideocontroller.md)
</dt> </dl>

 

 




