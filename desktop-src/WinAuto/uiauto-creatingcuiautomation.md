---
title: Crear el objeto CUIAutomation
description: En esta sección se describe cómo empezar a escribir una aplicación cliente de automatización de la interfaz de usuario de Microsoft mediante la creación de instancias de un objeto que implementa IUIAutomation.
ms.assetid: 9b90da60-0204-48c1-bb16-ff4a843bac67
keywords:
- clientes, crear objeto CUIAutomation
- clients, CUIAutomation, objeto
- Automatización de la interfaz de usuario, objeto CUIAutomation
- Automatización de la interfaz de usuario, crear objeto CUIAutomation
- creación de un objeto CUIAutomation
- Objeto CUIAutomation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8162dac5276bbb22d00413276482cca34334fda5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995313"
---
# <a name="creating-the-cuiautomation-object"></a>Crear el objeto CUIAutomation

En esta sección se describe cómo empezar a escribir una aplicación cliente de automatización de la interfaz de usuario de Microsoft mediante la creación de instancias de un objeto que implementa [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation).

En este tema se incluyen las siguientes secciones.

-   [El objeto CUIAutomation](#the-cuiautomation-object)
-   [Crear el objeto](#creating-the-object)
-   [Temas relacionados](#related-topics)

## <a name="the-cuiautomation-object"></a>El objeto CUIAutomation

El primer paso en el uso de la automatización de la interfaz de usuario es crear un objeto de la clase [**CUIAutomation**](/previous-versions/windows/desktop/legacy/ff384838(v=vs.85)) . Este objeto expone la interfaz [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) , que es la puerta de enlace a todos los demás objetos e interfaces que usan las aplicaciones cliente. Entre otras cosas, **IUIAutomation** se usa para las tareas siguientes:

-   Suscribirse a eventos.
-   Crear condiciones. Las condiciones son objetos que se utilizan para restringir el ámbito de las búsquedas de los elementos de automatización de la interfaz de usuario.
-   Obtener elementos de UI Automation directamente desde el escritorio (el elemento raíz) o desde las coordenadas de pantalla o los identificadores de ventana.
-   Crear objetos de rastreador de árbol que se pueden usar para navegar por la jerarquía de elementos de automatización de la interfaz de usuario.
-   Convertir tipos de datos.

## <a name="creating-the-object"></a>Crear el objeto

Para empezar a usar la automatización de la interfaz de usuario en su aplicación, siga estos pasos:

-   Incluya UIAutomation. h en los encabezados del proyecto. UIAutomation. h coloca en los otros encabezados que definen la API.
-   Declare un puntero a [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation).
-   Inicialice el modelo de objetos componentes (COM).
-   Cree una instancia de [**CUIAutomation**](/previous-versions/windows/desktop/legacy/ff384838(v=vs.85)) y recupere la interfaz [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) en el puntero.

La función de ejemplo siguiente inicializa COM y, a continuación, crea el objeto [**CUIAutomation**](/previous-versions/windows/desktop/legacy/ff384838(v=vs.85)) y recupera la interfaz [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) en el puntero *ppAutomation* .


```C++
#include <uiautomation.h>

// CoInitialize must be called before calling this function, and the  
// caller must release the returned pointer when finished with it.
// 
HRESULT InitializeUIAutomation(IUIAutomation **ppAutomation)
{
    return CoCreateInstance(CLSID_CUIAutomation, NULL,
        CLSCTX_INPROC_SERVER, IID_IUIAutomation, 
        reinterpret_cast<void**>(ppAutomation));
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Vista**
</dt> <dt>

[Información general sobre eventos de UI Automation](uiauto-eventsoverview.md)
</dt> <dt>

[Obtener elementos de UI Automation](uiauto-obtainingelements.md)
</dt> </dl>

 

 