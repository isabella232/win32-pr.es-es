---
title: Interfaz IWMDRMProvider
description: La interfaz IWMDRMProvider proporciona un método que crea los demás objetos de las API extendidas del cliente DRM de Microsoft Windows Media. Puede obtener un puntero a una instancia de esta interfaz llamando a la función WMDRMCreateProvider.
ms.assetid: bcd346e3-a79f-49a8-b5f9-b9ae8b54527a
keywords:
- Windows Media Format de la interfaz IWMDRMProvider
- IWMDRMProvider interface windows Media Format , descrito
topic_type:
- apiref
api_name:
- IWMDRMProvider
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bfe08a00d94914744f184ac4d0409fed24701985740006841f1d178cc39273e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119930125"
---
# <a name="iwmdrmprovider-interface"></a>Interfaz IWMDRMProvider

La **interfaz IWMDRMProvider proporciona** un método que crea los demás objetos de las API extendidas del cliente DRM de Microsoft Windows Media.

Puede obtener un puntero a una instancia de esta interfaz llamando a la [**función WMDRMCreateProvider.**](wmdrmcreateprovider.md) Para obtener un puntero a una instancia de esta interfaz que pueda crear objetos seguros, debe llamar a la [**función WMDRMCreateProtectedProvider.**](wmdrmcreateprotectedprovider.md)

## <a name="members"></a>Miembros

La **interfaz IWMDRMProvider** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IWMDRMProvider también** tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IWMDRMProvider tiene** estos métodos.



| Método                                              | Descripción                                                                                          |
|:----------------------------------------------------|:-----------------------------------------------------------------------------------------------------|
| [**Createobject**](iwmdrmprovider-createobject.md) | Recupera un puntero a una interfaz especificada y crea el objeto de implementación si es necesario.<br/> |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaces**](drm-interfaces.md)
</dt> </dl>

 

