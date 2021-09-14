---
description: Trabajar con menús de DVD
ms.assetid: 8c5f8072-b74f-4e15-8991-73bcc4145fd2
title: Trabajar con menús de DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 113647a37200762b5eaf0a9ac231dea74ad19925
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127272580"
---
# <a name="working-with-dvd-menus"></a>Trabajar con menús de DVD

El navegador de DVD puede mostrar un menú cuando el usuario activa un botón o cuando el navegador entra en el dominio De primera reproducción. Para mostrar un menú mediante programación, llame al [**método IDvdControl2::ShowMenu.**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-showmenu)

Hay varias maneras de seleccionar botones de menú mediante programación:

-   Para seleccionar un botón por número, llame a [**IDvdControl2::SelectButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectbutton). Los botones se numeran de 1 a 36. El [**método IDvdInfo2::GetCurrentButton**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcurrentbutton) devuelve el número de botones disponibles.
-   Para seleccionar un botón con respecto a la posición del botón seleccionado actualmente, llame a [**IDvdControl2::SelectRelativeButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectrelativebutton). Puede seleccionar un botón en la dirección arriba, abajo, izquierda o derecha.
-   Para seleccionar un botón por sus coordenadas dentro de la ventana, llame a [**IDvdControl2::SelectAtPosition**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectatposition). Este método toma (x,y) coordenadas relativas al área cliente de la ventana de vídeo. (Para el modo sin ventanas, esta es la ventana de la aplicación). Si no hay ningún botón en esa ubicación, el método devuelve VFW \_ E \_ DVD NO \_ \_ BUTTON.

Además, hay varias maneras de activar un botón:

-   Para activar un botón por número, llame a [**IDvdControl2::SelectAndActivateButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectandactivatebutton).
-   Para activar un botón por sus coordenadas, llame a [**IDvdControl2::ActivateAtPosition**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-activateatposition).
-   Para activar el botón que está seleccionado actualmente, llame a [**IDvdControl2::ActivateButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-activatebutton). Si no se selecciona ningún botón, el método devuelve VFW \_ E \_ DVD NO \_ \_ BUTTON.

Tenga en cuenta que la selección de un botón simplemente resalta sus bordes. Para hacer que se desactive el comando asociado, se debe activar el botón. La activación de un botón mediante programación se puede realizar de varias maneras, pero el botón siempre debe seleccionarse antes de que se pueda activar.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Aplicaciones de DVD](dvd-applications.md)
</dt> </dl>

 

 



