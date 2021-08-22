---
description: El método Reset de la clase NonVolatileStorage de CIM solicita \_ un restablecimiento del dispositivo lógico.
ms.assetid: 5fa02e46-4823-4ffa-b4e9-0930fed6fb03
ms.tgt_platform: multiple
title: Método Reset de la CIM_NonVolatileStorage clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_NonVolatileStorage.Reset
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: e8cd378cbff7e8c723d0e9dc7a99cf4a10ffce8b541ec46a5b8232d6e43937e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118418860"
---
# <a name="reset-method-of-the-cim_nonvolatilestorage-class"></a>Método Reset de la \_ clase NonVolatileStorage de CIM

El **método Reset** de la clase NonVolatileStorage de CIM solicita un \_ restablecimiento del dispositivo lógico. Este método se hereda de [**\_ CIM LogicalDevice.**](cim-logicaldevice.md)

> [!IMPORTANT]
> Las clases CIM (Modelo de información común) DMTF (Distributed Management Task Force) son las clases primarias en las que se han creado las clases WMI. WMI admite actualmente solo los esquemas [de la versión CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

## <a name="syntax"></a>Sintaxis


```mof
uint32 Reset();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve 0 (cero) si la solicitud se ejecutó correctamente, 1 (uno) si no se admite la solicitud y algún otro valor si se produjo un error.

## <a name="remarks"></a>Comentarios

Wmi no implementa actualmente este método. Para usar este método, debe implementarlo en su propio proveedor.

Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF. Microsoft puede haber realizado cambios para corregir errores menores, ajustarse a los estándares de documentación del SDK de Microsoft o proporcionar más información.

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

[CIM \_ NonVolatileStorage](reset-method-in-class-cim-nonvolatilestorage.md)
</dt> <dt>

[**CIM \_ NonVolatileStorage**](cim-nonvolatilestorage.md)
</dt> </dl>

 

 




