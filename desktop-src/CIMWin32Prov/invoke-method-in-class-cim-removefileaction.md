---
description: El método Invoke de la \_ clase CIM RemoveFileAction toma una acción concreta. Los detalles de cómo realiza la acción el método son específicos de la implementación. Este método se hereda de la \_ acción CIM.
ms.assetid: 7fc33654-a51b-41cf-a5b4-ef08fd6e40ac
ms.tgt_platform: multiple
title: Método Invoke de la clase CIM_RemoveFileAction
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_RemoveFileAction.Invoke
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a371ad1f7b1da874b6a049b04d5f50ec694cf181
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659463"
---
# <a name="invoke-method-of-the-cim_removefileaction-class"></a>Método Invoke de la \_ clase CIM RemoveFileAction

El método **Invoke** de la clase [**CIM \_ RemoveFileAction**](cim-removefileaction.md) toma una acción concreta. Los detalles de cómo realiza la acción el método son específicos de la implementación. Este método se hereda de [**la \_ acción CIM**](cim-action.md).

> [!IMPORTANT]
> Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI. WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

En este tema se usa la sintaxis de Managed Object Format (MOF). Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxis


```mof
uint32 Invoke();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de 0 (cero) si se realiza correctamente y cualquier otro número para indicar un error.

## <a name="remarks"></a>Observaciones

Este método no está implementado actualmente por WMI. Para usar este método, debe implementarlo en su propio proveedor.

Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF. Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | Origen de \\ cimv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[\_REMOVEFILEACTION CIM](invoke-method-in-class-cim-removefileaction.md)
</dt> <dt>

[**\_REMOVEFILEACTION CIM**](cim-removefileaction.md)
</dt> </dl>

 

