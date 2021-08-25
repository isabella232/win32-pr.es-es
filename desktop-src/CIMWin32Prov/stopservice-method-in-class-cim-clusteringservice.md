---
description: Detiene el servicio representado por el objeto derivado de CIM \_ ClusteringService.
ms.assetid: b8dbaeeb-819b-469b-9f5e-d658e88d1a6e
ms.tgt_platform: multiple
title: Método StopService de la CIM_ClusteringService (Sdoias.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ClusteringService.StopService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2c6cb636a644ba9d67bb6165163b297257af83753a1bcae77a0aa53f8731ffa3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119752305"
---
# <a name="stopservice-method-of-the-cim_clusteringservice-class"></a>Método StopService de la clase \_ ClusteringService de CIM

El **método StopService** detiene el servicio representado por el objeto derivado de [**CIM \_ ClusteringService**](cim-clusteringservice.md). Este método se hereda del [**servicio CIM. \_**](cim-service.md)

> [!IMPORTANT]
> Las clases CIM (Modelo de información común) DE DMTF (Distributed Management Task Force) son las clases primarias en las que se han creado las clases WMI. WMI admite actualmente solo los esquemas [de la versión CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

En este tema se usa Managed Object Format sintaxis de MOF. Para obtener más información sobre el uso de este método, vea [Llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxis


```mof
uint32 StopService();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de 0 (cero) si el servicio se detuvo correctamente, 1 (uno) si no se admite la solicitud y cualquier otro número para indicar un error.

## <a name="remarks"></a>Comentarios

Wmi no implementa actualmente este método. Para usar este método, debe implementarlo en su propio proveedor.

Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF. Microsoft puede haber realizado cambios para corregir errores menores, ajustarse a los estándares de documentación del SDK de Microsoft o proporcionar más información.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                  |
| Header<br/>                   | <dl> <dt>Sdoias.h</dt> </dl>     |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CIM \_ ClusteringService**](stopservice-method-in-class-cim-clusteringservice.md)
</dt> <dt>

[**CIM \_ ClusteringService**](cim-clusteringservice.md)
</dt> </dl>

 

