---
description: El método EvictNode quita un sistema informático de un clúster. El nodo que se va a expulsar se especifica como un parámetro para el método .
ms.assetid: 4691d536-ade3-4a02-bc28-e31ebaf5d9e4
ms.tgt_platform: multiple
title: Método EvictNode de la CIM_ClusteringService clase
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
ms.openlocfilehash: f5574548781f4ab5b7ecbc1ead08aba10ec0bfaf8c0740e2e429303732e90e88
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120077655"
---
# <a name="evictnode-method-of-the-cim_clusteringservice-class"></a>Método EvictNode de la clase \_ ClusteringService de CIM

El **método EvictNode** quita un sistema informático de un clúster. El nodo que se va a expulsar se especifica como un parámetro para el método .

> [!IMPORTANT]
> Las clases CIM (Modelo de información común) DMTF (Distributed Management Task Force) son las clases primarias en las que se construyen las clases WMI. WMI admite actualmente solo los esquemas [de versión CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

En este tema se usa Managed Object Format sintaxis MOF (MOF). Para obtener más información sobre el uso de este método, vea [Llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxis


```mof
uint32 EvictNode(
  [in] CIM_ComputerSystem REF CS
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*CS* \[ En\]
</dt> <dd>

Referencia al sistema del equipo que se quitará del clúster.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve 0 (cero) si el sistema del equipo se expulsa correctamente, 1 (uno) si no se admite el método y cualquier otro número si se produjo un error.

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

[**CIM \_ ClusteringService**](evictnode-method-in-class-cim-clusteringservice.md)
</dt> <dt>

[**CIM \_ ClusteringService**](cim-clusteringservice.md)
</dt> </dl>

 

