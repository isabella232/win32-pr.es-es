---
description: El método Invoke de la \_ clase CIM SoftwareElementVersionCheck evalúa una comprobación determinada.
ms.assetid: 5b477945-7ad4-49e2-b9c8-4a700a45f2b6
ms.tgt_platform: multiple
title: Método Invoke de la CIM_SoftwareElementVersionCheck clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SoftwareElementVersionCheck.Invoke
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2d65921a07dd6e5ab6df54ea1ba71117c58a18dc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167969"
---
# <a name="invoke-method-of-the-cim_softwareelementversioncheck-class"></a>Método Invoke de la \_ clase SoftwareElementVersionCheck de CIM

El **método Invoke** de la clase CIM [**\_ SoftwareElementVersionCheck**](cim-softwareelementversioncheck.md) evalúa una comprobación determinada. Los detalles de cómo el método evalúa una comprobación determinada en un contexto CIM se describen mediante las subclases [**cim \_ check**](cim-check.md) no abstractas. Este método se hereda de **CIM \_ Check**.

> [!IMPORTANT]
> Las clases CIM (Modelo de información común) DE DMTF (Distributed Management Task Force) son las clases primarias en las que se han creado las clases WMI. WMI admite actualmente solo los esquemas [de la versión CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

En este tema se usa Managed Object Format sintaxis de MOF. Para obtener más información sobre el uso de este método, vea [Llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxis


```mof
uint32 Invoke();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de 0 (cero) si se ejecuta correctamente y cualquier otro número para indicar un error.

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



## <a name="see-also"></a>Vea también

<dl> <dt>

[CIM \_ SoftwareElementVersionCheck](invoke-method-in-class-cim-softwareelementversioncheck.md)
</dt> <dt>

[**CIM \_ SoftwareElementVersionCheck**](cim-softwareelementversioncheck.md)
</dt> </dl>

 

