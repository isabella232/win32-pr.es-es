---
description: El método Invoke de la \_ clase CIM DirectorySpecification evalúa una comprobación determinada.
ms.assetid: 63289f94-f134-4159-898c-404cdd8f2a5c
ms.tgt_platform: multiple
title: Método Invoke de la clase CIM_DirectorySpecification
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DirectorySpecification.Invoke
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 48e5cb315f7dba6be187280ee6a16d7c4711752f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659470"
---
# <a name="invoke-method-of-the-cim_directoryspecification-class"></a>Método Invoke de la \_ clase CIM DirectorySpecification

El método **Invoke** de la clase [**CIM \_ DirectorySpecification**](cim-directoryspecification.md) evalúa una comprobación determinada. Los detalles sobre cómo evalúa el método una comprobación determinada en un contexto CIM se describen en las subclases [**de \_ comprobación CIM**](cim-check.md) no abstractas. Este método se hereda de **la \_ comprobación CIM**.

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

Devuelve 0 si se realiza correctamente, 1 si no se admite el método, y cualquier otro valor indica un error.

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

[\_DIRECTORYSPECIFICATION CIM](invoke-method-in-class-cim-directoryspecification.md)
</dt> <dt>

[**\_DIRECTORYSPECIFICATION CIM**](cim-directoryspecification.md)
</dt> </dl>

 

