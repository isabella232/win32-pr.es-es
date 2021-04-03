---
description: El método EvictNode quita un equipo de un clúster. El nodo que se va a expulsar se especifica como un parámetro para el método.
ms.assetid: 4691d536-ade3-4a02-bc28-e31ebaf5d9e4
ms.tgt_platform: multiple
title: Método EvictNode de la clase CIM_ClusteringService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ClusteringService.EvictNode
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: d68ddc1adc0af335dcf2d4139cf7c1f0a381d986
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807255"
---
# <a name="evictnode-method-of-the-cim_clusteringservice-class"></a>Método EvictNode de la \_ clase ClusteringService de CIM

El método **EvictNode** quita un equipo de un clúster. El nodo que se va a expulsar se especifica como un parámetro para el método.

> [!IMPORTANT]
> Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI. WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

En este tema se usa la sintaxis de Managed Object Format (MOF). Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxis


```mof
uint32 EvictNode(
  [in] CIM_ComputerSystem REF CS
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*CS* \[ de\]
</dt> <dd>

Referencia al sistema del equipo que se va a quitar del clúster.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve 0 (cero) si se expulsa correctamente el sistema del equipo, 1 (uno) si no se admite el método, y cualquier otro número si se produjo un error.

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

[**\_CLUSTERINGSERVICE CIM**](evictnode-method-in-class-cim-clusteringservice.md)
</dt> <dt>

[**\_CLUSTERINGSERVICE CIM**](cim-clusteringservice.md)
</dt> </dl>

 

