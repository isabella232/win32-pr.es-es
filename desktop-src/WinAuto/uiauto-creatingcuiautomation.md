---
title: Creación del objeto CUIAutomation
description: En esta sección se describe cómo empezar a escribir una aplicación cliente de Microsoft Automatización de la interfaz de usuario mediante la creación de instancias de un objeto que implementa IUIAutomation.
ms.assetid: 9b90da60-0204-48c1-bb16-ff4a843bac67
keywords:
- clients,creating CUIAutomation object
- clients,objeto CUIAutomation
- Automatización de la interfaz de usuario,objeto CUIAutomation
- Automatización de la interfaz de usuario, crear el objeto CUIAutomation
- crear el objeto CUIAutomation
- Objeto CUIAutomation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8b9720ce31f883c4561ae3f82372d902a0dcc3fbfca4bae6de998ce438a6d22
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119795495"
---
# <a name="creating-the-cuiautomation-object"></a>Creación del objeto CUIAutomation

En esta sección se describe cómo empezar a escribir una aplicación cliente de Microsoft Automatización de la interfaz de usuario mediante la creación de instancias de un objeto que implementa [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation).

En este tema se incluyen las siguientes secciones.

-   [El objeto CUIAutomation](#the-cuiautomation-object)
-   [Creación del objeto](#creating-the-object)
-   [Temas relacionados](#related-topics)

## <a name="the-cuiautomation-object"></a>El objeto CUIAutomation

El primer paso para usar Automatización de la interfaz de usuario es crear un objeto de la [**clase CUIAutomation.**](/previous-versions/windows/desktop/legacy/ff384838(v=vs.85)) Este objeto expone la [**interfaz IUIAutomation,**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) que es la puerta de enlace a todos los demás objetos e interfaces que usan las aplicaciones cliente. Entre otras cosas, **IUIAutomation** se usa para las tareas siguientes:

-   Suscribirse a eventos.
-   Crear condiciones. Las condiciones son objetos que se usan para restringir el ámbito de las búsquedas Automatización de la interfaz de usuario elementos.
-   Obtener Automatización de la interfaz de usuario elementos directamente desde el escritorio (el elemento raíz) o desde coordenadas de pantalla o identificadores de ventana.
-   Crear objetos de árbol que se pueden usar para navegar por la jerarquía de Automatización de la interfaz de usuario elementos.
-   Convertir tipos de datos.

## <a name="creating-the-object"></a>Creación del objeto

Para empezar a usar Automatización de la interfaz de usuario en la aplicación, siga estos pasos:

-   Incluya UIAutomation.h en los encabezados del proyecto. UIAutomation.h incluye los demás encabezados que definen la API.
-   Declare un puntero a [**IUIAutomation.**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation)
-   Inicialice el modelo de objetos componentes (COM).
-   Cree una instancia de [**CUIAutomation y**](/previous-versions/windows/desktop/legacy/ff384838(v=vs.85)) recupere la [**interfaz IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) en el puntero.

La función de ejemplo siguiente inicializa COM y, a continuación, crea el objeto [**CUIAutomation,**](/previous-versions/windows/desktop/legacy/ff384838(v=vs.85)) recuperando la [**interfaz IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) en el *puntero ppAutomation.*


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

**Conceptual**
</dt> <dt>

[Información general sobre eventos de UI Automation](uiauto-eventsoverview.md)
</dt> <dt>

[Obtener elementos de UI Automation](uiauto-obtainingelements.md)
</dt> </dl>

 

 