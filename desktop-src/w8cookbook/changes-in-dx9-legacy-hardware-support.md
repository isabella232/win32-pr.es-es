---
title: Cambios en la compatibilidad con hardware heredado de DX9
description: Cambios en la compatibilidad con hardware heredado de DX9
ms.assetid: 25C7DFC7-58F4-4F6D-8D26-6DBA92424A0B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bfd0b8bbb05161ffe14ff57cc5db97fe88a22bf6e64a495e2b43dd8240def82
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118211811"
---
# <a name="changes-in-dx9-legacy-hardware-support"></a>Cambios en la compatibilidad con hardware heredado de DX9

## <a name="platform"></a>Plataforma

**Clientes:** Windows 8 


## <a name="description"></a>Descripción

Intel y AMD/ATI ya no admiten sus partes gráficas DX9 y no actualizarán los controladores de estos dispositivos para Windows 8. Además, estos dispositivos no se tratan en la caja para Windows 8. Los últimos controladores para estos dispositivos son los disponibles en WU y en los sitios web de OEM/IHV. muchos de ellos datan de Vista y muchos de estos controladores de versión final presentan problemas en Windows 8. Además, nVidia ha indicado recientemente que no admitirán sus partes móviles dx9 (Vista y anteriores) (cuaderno) para Windows 8. Siguen siendo compatibles con sus partes DX9 de escritorio.

Todas estas combinaciones de controladores y partes están en la Internet Explorer de reserva de software 9. Esto significa que, por motivos de rendimiento o estabilidad, Internet Explorer 9 usa la representación de software en estos dispositivos. Esto es una buena indicación de que la experiencia con Windows Store no será satisfactoria en estos controladores y partes.

## <a name="manifestation"></a>Manifestación

Como no hay compatibilidad con estos dispositivos, muchos usuarios con estas partes se ejecutarán en el controlador de pantalla básico de Microsoft. Se trata de una GPU de software WDDM 1.2 basada en WARP y es realmente más rápida que algunas de las partes de esta clase, por ejemplo, la serie Intel GMA500. Admite avión y DWM, y puede ejecutar aplicaciones Windows Store.

Sin embargo, tiene algunas limitaciones importantes:

-   No admite varios monitores ni proyección
-   No admite la suspensión, aunque sí admite la hibernación
-   A menudo no permite cambiar la resolución de pantalla

## <a name="mitigation"></a>Mitigación

Si después de las pruebas, descubre que la experiencia del usuario no es aceptable, puede optar por establecer requisitos de hardware para sus productos que excluyan estas piezas de Intel y AMD de DX9 anteriores. También puede optar por alertar a los clientes de que pueden tener una experiencia inaceptable en estas partes.

## <a name="tests"></a>Pruebas

Evalúe el rendimiento y la experiencia en estos dispositivos:

-   ¿Cómo es la experiencia en la versión final del controlador disponible?
-   ¿Cómo es la experiencia en MSBDD?

 

 




