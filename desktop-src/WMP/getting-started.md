---
title: Introducción con el SDK de Windows Media Player
description: Introducción con el SDK de Windows Media Player
ms.assetid: 47c333dc-dad3-4430-a053-016d2c931f74
keywords:
- Windows Media Player Mobile, Complementos
- Windows Media Player Mobile, Complementos de la interfaz de usuario
- Complementos móviles de Windows Media Player
- complementos, interfaz de usuario
- complementos, Windows Media Player Mobile
- Complementos de la interfaz de usuario, Windows Media Player Mobile
- Complementos de la interfaz de usuario, Windows Media Player Mobile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a962c1f815f820a0b2e8125872baf9d02e301dc
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "103800626"
---
# <a name="getting-started-with-the-windows-media-player-sdk"></a>Introducción con el SDK de Windows Media Player

Para crear el complemento, primero debe instalar Microsoft eMbedded Visual C++ 4,0 y Visual Studio 2003. También debe instalar el SDK de Pocket PC 2003 o el SDK de smartphone 2003, que son descargas independientes. Para compilar y ejecutar el proyecto, un dispositivo Pocket PC o smartphone que ejecute el sistema operativo Windows Mobile 2003 Second Edition debe estar sincronizado con el equipo de desarrollo mediante Microsoft ActiveSync® 3.7.1 o posterior.

Dado que los complementos de interfaz de usuario en dispositivos Windows Mobile usan el mismo modelo de complemento que las versiones de escritorio, puede usar el Asistente para complementos de Windows Media Player como punto de partida al crear un complemento de la interfaz de usuario de fondo que funcionará con Windows Media Player 10 Mobile.

Para crear código de complemento de la interfaz de usuario, haga lo siguiente:

1.  Abra Visual Studio 2003 e inicie un nuevo proyecto en Visual C++.
2.  En el panel **plantillas** **, seleccione Asistente para complementos de Media Player de Windows** .
3.  Asigne al proyecto el nombre NetworkPlugin y haga clic en **Aceptar**.
4.  Seleccione **complemento** de la interfaz de usuario y haga clic en **siguiente**.
5.  Seleccione **fondo** y haga clic en **siguiente**.
6.  Haga clic en **Siguiente** para cerrar el asistente. Si va a supervisar eventos con el complemento, debe comprobar la **escucha de eventos** antes de finalizar el asistente, y debe leer la documentación de la interfaz **IWMPEvents** para averiguar qué eventos se admiten en Windows Media Player 10 Mobile.

Ahora que ha creado el código de complemento de la interfaz de usuario, debe crear un proyecto Windows CE DLL vacío en eMbedded Visual C++ 4,0. Después, copie los archivos de código fuente generados por el asistente en ese nuevo proyecto para que se compilen con el compilador ARM4.

Para crear un proyecto vacío

1.  Inicie un nuevo proyecto en el Visual C++ incrustado y, a continuación, seleccione **WCE Dynamic-Link Library** en el panel **proyectos** .
2.  Asigne un nombre al proyecto y haga clic en **Aceptar**.
3.  Asegúrese de que haya seleccionado **un proyecto Windows CE dll vacío** y, a continuación, haga clic en **Finalizar**.
4.  Haga clic en el elemento de menú **proyecto** .
5.  Seleccione **Agregar al proyecto** y, a continuación, haga clic en **archivos**.
6.  Seleccione los archivos de C++ que creó con el Asistente para complementos y, a continuación, haga clic en **Aceptar**.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Crear un complemento de la interfaz de usuario para Windows Media Player 10 Mobile**](creating-a-user-interface-plug-in-for-windows-media-player-10-mobile.md)
</dt> <dt>

[**Interfaz IWMPEvents**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents)
</dt> </dl>

 

 




