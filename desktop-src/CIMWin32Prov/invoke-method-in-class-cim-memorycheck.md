---
description: El método Invoke de la clase MemoryCheck de CIM \_ evalúa una comprobación determinada. Los detalles de cómo el método evalúa una comprobación determinada en un contexto CIM se describen mediante las subclases cim check no \_ abstractas. Este método se hereda de CIM \_ Check.
ms.assetid: 264a7690-b066-4024-8cb1-d988b829dc72
ms.tgt_platform: multiple
title: Método Invoke de la CIM_MemoryCheck clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MemoryCheck.Invoke
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1607d6b6db173b79db19584444b6928fc0e87b9ecf11e39b9e67e34acdb29496
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120003665"
---
# <a name="invoke-method-of-the-cim_memorycheck-class"></a>Método Invoke de la clase \_ MemoryCheck de CIM

El **método Invoke** de la clase [**\_ MemoryCheck de CIM**](cim-memorycheck.md) evalúa una comprobación determinada. Los detalles de cómo el método evalúa una comprobación determinada en un contexto CIM se describen mediante las subclases [**cim \_ check**](cim-check.md) no abstractas. Este método se hereda de **CIM \_ Check**.

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

Devuelve un valor de 0 (cero) si se ejecuta correctamente y cualquier otro número para indicar un error.

## <a name="remarks"></a>Comentarios

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



## <a name="see-also"></a>Vea también

<dl> <dt>

[CIM \_ MemoryCheck](invoke-method-in-class-cim-memorycheck.md)
</dt> <dt>

[**Comprobación de memoria de CIM \_**](cim-memorycheck.md)
</dt> </dl>

 

