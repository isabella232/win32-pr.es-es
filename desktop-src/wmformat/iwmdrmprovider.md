---
title: Interfaz IWMDRMProvider
description: La interfaz IWMDRMProvider proporciona un método que crea los demás objetos de las API extendidas del cliente DRM de Microsoft Windows Media. puede obtener un puntero a una instancia de esta interfaz mediante una llamada a la función WMDRMCreateProvider.
ms.assetid: bcd346e3-a79f-49a8-b5f9-b9ae8b54527a
keywords:
- Interfaz IWMDRMProvider formato de Windows Media
- Interfaz IWMDRMProvider formato de Windows Media, descrito
topic_type:
- apiref
api_name:
- IWMDRMProvider
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9653bc612cdbc865d8e77cb7916b0b8f54d0fd0e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793060"
---
# <a name="iwmdrmprovider-interface"></a>Interfaz IWMDRMProvider

La interfaz **IWMDRMProvider** proporciona un método que crea los demás objetos de las API extendidas del cliente DRM de Microsoft Windows Media.

Puede obtener un puntero a una instancia de esta interfaz mediante una llamada a la función [**WMDRMCreateProvider**](wmdrmcreateprovider.md) . Para obtener un puntero a una instancia de esta interfaz que pueda crear objetos seguros, debe llamar a la función [**WMDRMCreateProtectedProvider**](wmdrmcreateprotectedprovider.md) .

## <a name="members"></a>Miembros

La interfaz **IWMDRMProvider** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IWMDRMProvider** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IWMDRMProvider** tiene estos métodos.



| Método                                              | Descripción                                                                                          |
|:----------------------------------------------------|:-----------------------------------------------------------------------------------------------------|
| [**DataSpace**](iwmdrmprovider-createobject.md) | Recupera un puntero a una interfaz especificada y crea el objeto de implementación si es necesario.<br/> |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaces**](drm-interfaces.md)
</dt> </dl>

 

