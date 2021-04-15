---
title: Cambios en la compatibilidad con hardware heredado de DX9
description: Cambios en la compatibilidad con hardware heredado de DX9
ms.assetid: 25C7DFC7-58F4-4F6D-8D26-6DBA92424A0B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc1ae5c4b15a2019450cc5b209f34561d8ec672d
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/01/2020
ms.locfileid: "105695776"
---
# <a name="changes-in-dx9-legacy-hardware-support"></a>Cambios en la compatibilidad con hardware heredado de DX9

## <a name="platform"></a>Plataforma

**Clientes** : Windows 8 


## <a name="description"></a>Descripción

Intel y AMD/ATI ya no admiten las piezas de gráficos de DX9 y no actualizarán los controladores de estos dispositivos para Windows 8. Además, estos dispositivos no se incluyen en la caja para Windows 8. Los últimos controladores de estos dispositivos son los disponibles en WU y en los sitios web de OEM/IHV; muchas fechas de vista y muchos de estos controladores de versión finales muestran problemas en Windows 8. Además, nVidia ha indicado recientemente que no admitirán sus componentes móviles de DX9 (vista y anterior) para Windows 8. Continúan admitiendo sus componentes de su escritorio.

Todas estas combinaciones de controlador/parte se encuentran en la lista de reserva de software de Internet Explorer 9. Esto significa que, por motivos de rendimiento o de estabilidad, Internet Explorer 9 usa la representación de software en estos dispositivos. Esta es una buena indicación de que la experiencia con las aplicaciones de la tienda Windows no será satisfactoria en estos controladores y partes.

## <a name="manifestation"></a>Manifestación

Como no hay compatibilidad integrada para estos dispositivos, muchos usuarios con estas partes se cargarán en ejecución en el controlador de pantalla básico de Microsoft. Se trata de una GPU de software WDDM 1,2 basada en WARP y, en realidad, es más rápida que algunas de las partes de esta clase, por ejemplo, la serie GMA500 de Intel). Admite Aero-Glass y DWM, y puede ejecutar aplicaciones de la tienda Windows.

Sin embargo, tiene algunas limitaciones importantes:

-   No admite varios monitores o proyección
-   No admite la suspensión, aunque admite la hibernación
-   A menudo, no permite cambiar la resolución de la pantalla.

## <a name="mitigation"></a>Mitigación

Si después de la prueba, observa que la experiencia del usuario no es aceptable, puede elegir establecer los requisitos de hardware para sus productos que excluyan estas piezas antiguas de Intel y AMD. También puede optar por avisar a los clientes de que pueden tener una experiencia inaceptable en estas partes.

## <a name="tests"></a>Pruebas

Evalúe el rendimiento y la experiencia en estos dispositivos:

-   ¿Cuál es la experiencia como en la versión de controlador final disponible?
-   ¿Cuál es la experiencia como en el MSBDD?

 

 




