---
description: Representa la característica de reasociación del historial de archivos, que permite a un usuario restablecer una relación con un destino de copia de seguridad utilizado por el mismo usuario en el pasado. La reasociación se realiza mediante una llamada a los métodos de la interfaz IFhReassociation.
ms.assetid: BB81F8ED-4DFB-4FA5-B3ED-ACBAB32BBE3D
title: Clase FhReassociation (Fhcfg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FhReassociation
api_type:
- COM
api_location:
- Fhcfg.idl
ms.openlocfilehash: 1e303799a792e788fcb948ad6d3c6e2fd732e26e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659535"
---
# <a name="fhreassociation-class"></a>Clase FhReassociation

Representa la característica de reasociación del historial de archivos, que permite a un usuario restablecer una relación con un destino de copia de seguridad utilizado por el mismo usuario en el pasado. La reasociación se realiza mediante una llamada a los métodos de la interfaz [**IFhReassociation**](/windows/desktop/api/Fhcfg/nn-fhcfg-ifhreassociation) .

## <a name="when-to-implement"></a>Cuándo implementar

La API del historial de archivos implementa esta clase. Para crear una instancia de esta clase, use la función [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Fhcfg. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Fhcfg. idl</dt> </dl> |



 

 
