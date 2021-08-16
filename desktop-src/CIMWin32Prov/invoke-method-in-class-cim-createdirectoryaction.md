---
description: El método Invoke de la \_ clase CreateDirectoryAction de CIM realiza una acción determinada. Los detalles sobre cómo el método realiza la acción son específicos de la implementación. Este método se hereda de la acción \_ CIM.
ms.assetid: f14e215d-31f2-46c5-b45e-3de64ce46bf2
ms.tgt_platform: multiple
title: Método Invoke de la CIM_CreateDirectoryAction clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CreateDirectoryAction.Invoke
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5d2c1a79a7a662dc7c0896cec4a7c1b99248fe8538c9b7cd07203366541a6830
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119080009"
---
# <a name="invoke-method-of-the-cim_createdirectoryaction-class"></a>Método Invoke de la \_ clase CreateDirectoryAction de CIM

El **método Invoke** de la clase [**\_ CreateDirectoryAction de CIM**](cim-createdirectoryaction.md) realiza una acción determinada. Los detalles sobre cómo el método realiza la acción son específicos de la implementación. Este método se hereda de la [**acción \_ CIM**](cim-action.md).

> [!IMPORTANT]
> Las clases CIM (Modelo de información común) DMTF (Distributed Management Task Force) son las clases primarias en las que se construyen las clases WMI. WMI admite actualmente solo los esquemas [de versión CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

En este tema se usa Managed Object Format sintaxis MOF (MOF). Para obtener más información sobre el uso de este método, vea [Llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxis


```mof
uint32 Invoke();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de 0 si se ejecuta correctamente y cualquier otro número para indicar un error.

## <a name="remarks"></a>Comentarios

Wmi no implementa actualmente este método. Para usar este método, debe implementarlo en su propio proveedor.

Esta documentación se deriva de las descripciones de clases CIM publicadas por dmtf. Microsoft puede haber realizado cambios para corregir errores menores, ajustarse a los estándares de documentación del SDK de Microsoft o proporcionar más información.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CreateDirectoryAction de CIM \_**](invoke-method-in-class-cim-createdirectoryaction.md)
</dt> <dt>

[**CreateDirectoryAction de CIM \_**](cim-createdirectoryaction.md)
</dt> </dl>

 

