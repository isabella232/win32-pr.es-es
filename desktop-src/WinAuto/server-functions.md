---
title: Funciones del servidor (Windows de accesibilidad)
description: Funciones de servidor
ms.assetid: 3cfa42c4-3d8b-44a1-9b8e-19248da12334
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10a747c073e84049fe578d19561b25d0b754dbb9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127567376"
---
# <a name="server-functions-windows-accessibility-features"></a>Funciones del servidor (Windows de accesibilidad)

Esta sección contiene información sobre las funciones de servidor usadas con Microsoft Active Accessibility.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                     | Descripción                                                                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AccNotifyTouchInteraction**](/windows/desktop/api/Oleacc/nf-oleacc-accnotifytouchinteraction)<br/> | Permite que una aplicación de tecnología de asistencia (AT) notifique al sistema que interactúa con la interfaz de usuario a través de una API de automatización de Windows (como Microsoft Automatización de la interfaz de usuario) como resultado de un gesto táctil del usuario. Esto permite que la tecnología de asistencia notifique a la aplicación de destino y al sistema que el usuario está interactuando con la interacción táctil.<br/> |
| [**AccSetRunningUtilityState**](/windows/desktop/api/Oleacc/nf-oleacc-accsetrunningutilitystate)<br/> | Establece valores del sistema que indican si el estado actual de una aplicación de tecnología de asistencia (AT) afecta a la funcionalidad que normalmente proporciona el sistema. <br/>                                                                                                                                                                                 |
| [**CreateStdAccessibleObject**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleobject)<br/> | Crea un objeto accesible con los métodos y propiedades del tipo especificado de elemento de interfaz de usuario proporcionado por el sistema.<br/>                                                                                                                                                                                                                      |
| [**CreateStdAccessibleProxy**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleproxya)<br/>   | Crea un objeto accesible que tiene las propiedades y métodos de la clase especificada del elemento de interfaz de usuario proporcionado por el sistema.<br/>                                                                                                                                                                                                                 |
| [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject)<br/>                 | Devuelve una referencia, similar a un identificador, al objeto especificado. Los servidores devuelven esta referencia al controlar [**WM \_ GETOBJECT**](wm-getobject.md).<br/>                                                                                                                                                                                              |
| [**ObjectFromLresult**](/windows/desktop/api/Oleacc/nf-oleacc-objectfromlresult)<br/>                 | Recupera un puntero de interfaz solicitado para un objeto accesible basado en una referencia de objeto generada previamente.<br/> Esta función está diseñada para uso interno por Microsoft Active Accessibility y se documenta solo con fines informativos. Ni los clientes ni los servidores deben llamar a esta función.<br/>                               |
| [**IsWinEventHookInstalled**](/windows/desktop/api/Winuser/nf-winuser-iswineventhookinstalled)<br/>     | Determina si hay un enlace de WinEvent instalado que podría recibir una notificación de un evento especificado.<br/>                                                                                                                                                                                                                                                |
| [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent)<br/>                       | Indica al sistema que se ha producido un evento predefinido. Si alguna aplicación cliente ha registrado una función de enlace para el evento, el sistema llama a la función de enlace del cliente.<br/>                                                                                                                                                                        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Active Accessibility Interfaz de usuario Services](active-accessibility-user-interface-services-ref.md)
</dt> </dl>

 

 





