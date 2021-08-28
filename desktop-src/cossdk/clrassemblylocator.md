---
description: Recupera información sobre un ensamblado cuando se usa código administrado en la .NET Framework Common Language Runtime.
ms.assetid: 45dcdc6a-74df-4763-ba8b-82f604db78d4
title: Clase ClrAssemblyLocator (ComSvcs.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ClrAssemblyLocator
api_type:
- COM
ms.openlocfilehash: 78f041e8bdc614b1ac6007e21ffbf46ea4afe789a501bb1acefdd21263031859
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129277"
---
# <a name="clrassemblylocator-class"></a>ClrAssemblyLocator (clase)

Recupera información sobre un ensamblado cuando se usa código administrado en la .NET Framework Common Language Runtime.

## <a name="when-to-implement"></a>Cuándo implementar

ESTA clase se implementa mediante COM+.



| Requisito | Value |
|------------|-------------------------------------------------------|
| CLSID      | GUID \_ AssemblyLocator                                 |
| ProgID     | L"System.EnterpriseServices.Internal.AssemblyLocator" |
| Interfaces | [**IAssemblyLocator**](/windows/desktop/api/ComSvcs/nn-comsvcs-iassemblylocator)          |



 

## <a name="when-to-use"></a>Cuándo se usa

Use esta clase para tener acceso a los métodos [**de IAssemblyLocator**](/windows/desktop/api/ComSvcs/nn-comsvcs-iassemblylocator).

## <a name="remarks"></a>Comentarios

Para crear este objeto, llame a [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).

Para usar esta clase de Microsoft Visual Basic, agregue una referencia a la biblioteca de tipos de servicios COM+. Un objeto ClrAssemblyLocator se puede declarar mediante "COMSVCSLib.ClrAssemblyLocator" como nombre de clase.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP solo con aplicaciones de escritorio de SP1 \[\]<br/>                                 |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                 |
| Header<br/>                   | <dl> <dt>ComSvcs.h</dt> </dl> |



 

