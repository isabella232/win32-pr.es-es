---
description: El método Invoke de la \_ clase de comprobación CIM evalúa una comprobación determinada.
ms.assetid: cf1adeb2-f8a2-4f84-978f-e801bce104ac
ms.tgt_platform: multiple
title: Método Invoke de la clase CIM_Check
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Check.Invoke
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7774fcd1b3ef451fffb34ce9ad10d404e8ea95b3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659471"
---
# <a name="invoke-method-of-the-cim_check-class"></a>Método Invoke de la \_ clase de comprobación CIM

El método **Invoke** de la clase de [**\_ comprobación CIM**](cim-check.md) evalúa una comprobación determinada.

Para obtener más información sobre cómo el método evalúa una comprobación determinada en un contexto CIM, vea las subclases [**de \_ comprobación de CIM**](cim-check.md) no abstractas.

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

Devuelve un valor de 0 (cero) si se realiza correctamente, 1 (uno) si no se admite el método, y cualquier otro número para indicar un error.

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

[**Comprobación de CIM \_**](invoke-method-in-class-cim-check.md)
</dt> <dt>

[**Comprobación de CIM \_**](cim-check.md)
</dt> </dl>

 

