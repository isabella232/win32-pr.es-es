---
description: El método Invoke de la \_ clase CIM Check evalúa una comprobación determinada.
ms.assetid: cf1adeb2-f8a2-4f84-978f-e801bce104ac
ms.tgt_platform: multiple
title: Método Invoke de la CIM_Check clase
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
ms.openlocfilehash: 68a6c03fbad6002d20f7ab84ac5aea3f7205183b613b66cd18d7cdf8b03678ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118958980"
---
# <a name="invoke-method-of-the-cim_check-class"></a>Método Invoke de la clase \_ CIM Check

El **método Invoke** de la clase CIM [**\_ Check**](cim-check.md) evalúa una comprobación determinada.

Para obtener más información sobre cómo el método evalúa una comprobación determinada en un contexto CIM, vea las subclases [**cim \_ check**](cim-check.md) no abstractas.

> [!IMPORTANT]
> Las clases CIM (Modelo de información común) DMTF (Distributed Management Task Force) son las clases primarias en las que se han creado las clases WMI. WMI admite actualmente solo los esquemas [de versión CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

En este tema se Managed Object Format sintaxis de MOF. Para obtener más información sobre el uso de este método, vea [Llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxis


```mof
uint32 Invoke();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de 0 (cero) si se ejecuta correctamente, 1 (uno) si no se admite el método y cualquier otro número para indicar un error.

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

[**Comprobación de \_ CIM**](invoke-method-in-class-cim-check.md)
</dt> <dt>

[**Comprobación de \_ CIM**](cim-check.md)
</dt> </dl>

 

