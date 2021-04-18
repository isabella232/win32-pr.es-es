---
description: Interfaz implementada por el cliente que permite a los desarrolladores proporcionar sus propias credenciales de forma dinámica en tiempo de ejecución para autenticar los contenedores no Unidos a un dominio con Active Directory.
title: Interfaz ICcgDomainAuthCredentials (ccgplugins. h)
ms.topic: reference
ms.date: 10/20/2020
topic_type:
- APIRef
- kbSyntax
api_name:
- ICcgDomainAuthCredentials
api_type:
- COM
api_location:
- ccgplugins.dll
ms.openlocfilehash: 8217f806ff0a1a6b38d045c7f665758ccaf8b1f5
ms.sourcegitcommit: 3d9dce1bd6c84e2b51759e940aa95aa9b459cd20
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/04/2021
ms.locfileid: "105721361"
---
# <a name="iccgdomainauthcredentials-interface"></a>Interfaz ICcgDomainAuthCredentials

Interfaz implementada por el cliente que permite a los desarrolladores proporcionar sus propias credenciales de forma dinámica en tiempo de ejecución para autenticar los contenedores no Unidos a un dominio con Active Directory. 

## <a name="members"></a>Miembros

La interfaz **ICcgDomainAuthCredentials** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ICcgDomainAuthCredentials** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **ICcgDomainAuthCredentials** tiene estos métodos.



| Método                                           | Descripción                                                                                               |
|:-------------------------------------------------|:----------------------------------------------------------------------------------------------------------|
| [**GetPasswordCredentials**](iccgdomainauthcredentials-getpasswordcredentials.md)               | Devuelve las credenciales para autenticar un contenedor no unido a un dominio con Active Directory.<br/>                                                              |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                             |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>ccgplugins. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>ccgplugins. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>ccgplugins.dll</dt> </dl> |
| IID<br/>                      | 6ecda518-2010-4437-8bc3-46e752b7b172<br/>          |



 

