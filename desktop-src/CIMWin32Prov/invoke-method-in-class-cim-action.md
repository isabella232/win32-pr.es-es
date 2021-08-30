---
description: El método Invoke de la clase Acción CIM \_ realiza una acción determinada. Los detalles de cómo el método realiza la acción son específicos de la implementación.
ms.assetid: 4f0be560-bd78-4c7f-b6e3-ca86837a84f9
ms.tgt_platform: multiple
title: Método Invoke de la CIM_Action clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Action.Invoke
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 383bfb17f2bb40ce063c86c56ad30afe0fc741742bf77939c6d56bbe4c816ac8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119760275"
---
# <a name="invoke-method-of-the-cim_action-class"></a>Método Invoke de la clase \_ Action de CIM

El **método Invoke** de la clase [**\_ Acción CIM**](cim-action.md) realiza una acción determinada. Los detalles de cómo el método realiza la acción son específicos de la implementación.

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



## <a name="see-also"></a>Vea también

<dl> <dt>

[Acción \_ cim](invoke-method-in-class-cim-action.md)
</dt> <dt>

[**Acción \_ cim**](cim-action.md)
</dt> <dt>

[Clases CIM](/windows/desktop/WmiSdk/cimclas)
</dt> </dl>

 

