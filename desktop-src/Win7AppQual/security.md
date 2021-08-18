---
description: Seguridad (Windows guía de calidad de aplicaciones Windows Server 2008 R2 y 7)
ms.assetid: 87331C1D-F468-4CA4-92BD-D4E5D4E930BC
title: Seguridad (Windows guía de calidad de aplicaciones Windows Server 2008 R2 y 7)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d392f5bf14997962173b9054baba861003877d851d6bd62a947b15757feec23
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994665"
---
# <a name="security-windows-7-and-windows-server-2008-r2-application-quality-cookbook"></a>Seguridad (Windows guía de calidad de aplicaciones Windows Server 2008 R2 y 7)

A partir de Windows Internet Explorer 7, Windows Internet Explorer se ejecuta  en un contexto de seguridad denominado Modo protegido cuando los usuarios lo ejecutan en el sistema operativo Windows Vista o en una versión posterior. Este modo se Internet Explorer en una configuración con privilegios inferiores a una aplicación de usuario estándar, por lo que cierta funcionalidad es limitada, especialmente ActiveX controles y determinados tipos de complementos. Para obtener más información sobre el modo protegido en Internet Explorer y su impacto en la compatibilidad, vea Descripción y trabajo en modo [protegido Internet Explorer](/previous-versions/windows/internet-explorer/ie-developer/) en MSDN Library.

De forma predeterminada, Windows Internet Explorer 8 también habilita la prevención de ejecución de datos (DEP), que ayuda a las aplicaciones a evitar la ejecución de código arbitrario en ataques en línea. Sin embargo, es posible que algunos complementos no usen esta característica de seguridad (por ejemplo, los complementos que no están diseñados para ejecutar solo el código que se encuentra en la memoria que se ha marcado específicamente como ejecutable, como las aplicaciones que se han creado mediante una versión anterior del marco de la biblioteca de plantillas de ActiveX (ATL).

Internet Explorer 8 también protege a los usuarios frente a posibles vulnerabilidades de seguridad que usan scripts. Por ejemplo, no puede navegar desde una dirección URL de una zona de menos confianza a una dirección URL de una zona de mayor confianza, excepto a través de la interacción explícita del usuario. Tampoco puede ocultar determinados elementos de la interfaz de usuario del explorador (como la barra de direcciones) en una zona de no confianza (Internet).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Diseñar actualizaciones que afectan a la compatibilidad entre exploradores](design-updates-that-impact-compatibility-between-browsers.md)
</dt> </dl>

 

 
