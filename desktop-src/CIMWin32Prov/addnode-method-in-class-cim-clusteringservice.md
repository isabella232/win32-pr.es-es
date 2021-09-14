---
description: Incorpora un nuevo sistema informático a un clúster.
ms.assetid: 26d9428e-99de-4dcb-96ed-d773f28e015a
ms.tgt_platform: multiple
title: Método AddNode de la CIM_ClusteringService clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ClusteringService.AddNode
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1769ebb876fd2ae99c800a61b80d339a850ab232
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126970359"
---
# <a name="addnode-method-of-the-cim_clusteringservice-class"></a>Método AddNode de la clase \_ ClusteringService de CIM

El **método AddNode** incorpora un nuevo sistema informático a un clúster. El nodo que se va a agregar se especifica como un parámetro para el método .

> [!IMPORTANT]
> Las clases CIM (Modelo de información común) DE DMTF (Distributed Management Task Force) son las clases primarias en las que se han creado las clases WMI. WMI admite actualmente solo los esquemas [de la versión CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

En este tema se Managed Object Format sintaxis de MOF. Para obtener más información sobre el uso de este método, vea [Llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxis


```mof
uint32 AddNode(
  [in] CIM_ComputerSystem REF CS
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*CS* \[ En\]
</dt> <dd>

Referencia al sistema informático que se agregará al clúster.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de 0 (cero) si se ejecuta correctamente, 1 (uno) si no se admite la operación y cualquier otro número para indicar un error.

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



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CIM \_ ClusteringService**](addnode-method-in-class-cim-clusteringservice.md)
</dt> <dt>

[**CIM \_ ClusteringService**](cim-clusteringservice.md)
</dt> </dl>

 

