---
title: Funciones de servidor (características de accesibilidad de Windows)
description: Funciones de servidor
ms.assetid: 3cfa42c4-3d8b-44a1-9b8e-19248da12334
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10a747c073e84049fe578d19561b25d0b754dbb9
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104421873"
---
# <a name="server-functions-windows-accessibility-features"></a>Funciones de servidor (características de accesibilidad de Windows)

Esta sección contiene información acerca de las funciones de servidor que se usan con Microsoft Active Accessibility.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                     | Descripción                                                                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AccNotifyTouchInteraction**](/windows/desktop/api/Oleacc/nf-oleacc-accnotifytouchinteraction)<br/> | Permite que una aplicación de tecnología de asistencia (AT) notifique al sistema que está interactuando con la interfaz de usuario a través de una API de automatización de Windows (como la automatización de la interfaz de usuario de Microsoft) como resultado de un gesto táctil del usuario. Esto permite que la tecnología de asistencia notifique a la aplicación de destino y al sistema que está interactuando con el usuario táctil.<br/> |
| [**AccSetRunningUtilityState**](/windows/desktop/api/Oleacc/nf-oleacc-accsetrunningutilitystate)<br/> | Establece valores del sistema que indican si el estado actual de una aplicación de tecnología de asistencia (AT) afecta a la funcionalidad que normalmente proporciona el sistema. <br/>                                                                                                                                                                                 |
| [**CreateStdAccessibleObject**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleobject)<br/> | Crea un objeto accesible con los métodos y las propiedades del tipo especificado del elemento de la interfaz de usuario proporcionado por el sistema.<br/>                                                                                                                                                                                                                      |
| [**CreateStdAccessibleProxy**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleproxya)<br/>   | Crea un objeto accesible que tiene las propiedades y los métodos de la clase especificada del elemento de la interfaz de usuario proporcionado por el sistema.<br/>                                                                                                                                                                                                                 |
| [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject)<br/>                 | Devuelve una referencia, similar a un identificador, al objeto especificado. Los servidores devuelven esta referencia al controlar [**WM \_ GETOBJECT**](wm-getobject.md).<br/>                                                                                                                                                                                              |
| [**ObjectFromLresult**](/windows/desktop/api/Oleacc/nf-oleacc-objectfromlresult)<br/>                 | Recupera un puntero de interfaz solicitado para un objeto accesible basado en una referencia de objeto previamente generada.<br/> Esta función está diseñada para uso interno de Microsoft Active Accessibility y se documenta únicamente con fines informativos. Ni los clientes ni los servidores deben llamar a esta función.<br/>                               |
| [**IsWinEventHookInstalled**](/windows/desktop/api/Winuser/nf-winuser-iswineventhookinstalled)<br/>     | Determina si hay un enlace WinEvent instalado que podría recibir una notificación de un evento especificado.<br/>                                                                                                                                                                                                                                                |
| [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent)<br/>                       | Indica al sistema que se ha producido un evento predefinido. Si alguna aplicación cliente ha registrado una función de enlace para el evento, el sistema llama a la función de enlace del cliente.<br/>                                                                                                                                                                        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Active Accessibility servicios de la interfaz de usuario](active-accessibility-user-interface-services-ref.md)
</dt> </dl>

 

 





