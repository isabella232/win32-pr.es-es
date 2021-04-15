---
description: Trabajar con menús de DVD
ms.assetid: 8c5f8072-b74f-4e15-8991-73bcc4145fd2
title: Trabajar con menús de DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 113647a37200762b5eaf0a9ac231dea74ad19925
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105689594"
---
# <a name="working-with-dvd-menus"></a>Trabajar con menús de DVD

El navegador de DVD puede mostrar un menú cuando el usuario activa un botón o cuando el navegador entra en el primer dominio de reproducción. Para mostrar un menú mediante programación, llame al método [**IDvdControl2:: showmenu**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-showmenu) .

Hay varias maneras de seleccionar botones de menú mediante programación:

-   Para seleccionar un botón por número, llame a [**IDvdControl2:: SelectButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectbutton). Los botones se numeran del 1 al 36. El método [**IDvdInfo2:: GetCurrentButton**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcurrentbutton) devuelve el número de botones disponibles.
-   Para seleccionar un botón relativo a la posición del botón seleccionado actualmente, llame a [**IDvdControl2:: SelectRelativeButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectrelativebutton). Puede seleccionar un botón en la dirección arriba, abajo, izquierda o derecha.
-   Para seleccionar un botón por sus coordenadas dentro de la ventana, llame a [**IDvdControl2:: SelectAtPosition**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectatposition). Este método toma las coordenadas (x, y) relativas al área cliente de la ventana de vídeo. (Para el modo sin ventanas, esta es la ventana de la aplicación). Si no hay ningún botón en esa ubicación, el método devuelve el \_ botón VFW E \_ DVD \_ no \_ .

Además, hay varias maneras de activar un botón:

-   Para activar un botón por número, llame a [**IDvdControl2:: SelectAndActivateButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectandactivatebutton).
-   Para activar un botón por sus coordenadas, llame a [**IDvdControl2:: ActivateAtPosition**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-activateatposition).
-   Para activar el botón que está seleccionado actualmente, llame a [**IDvdControl2:: ActivateButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-activatebutton). Si no se selecciona ningún botón, el método devuelve \_ el \_ botón VFW E DVD \_ no \_ .

Tenga en cuenta que la selección de un botón simplemente resalta los bordes. Para que se desencadene el comando asociado, se debe activar el botón. La activación de un botón mediante programación se puede realizar de varias maneras, pero el botón siempre debe estar seleccionado antes de que se pueda activar.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Aplicaciones de DVD](dvd-applications.md)
</dt> </dl>

 

 



