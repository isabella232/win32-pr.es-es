---
description: .
ms.assetid: 87331C1D-F468-4CA4-92BD-D4E5D4E930BC
title: Seguridad (Guía de calidad de la aplicación Windows 7 y Windows Server 2008 R2)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bbaaa6b34463e04f5870082e5c693462f4e19fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279632"
---
# <a name="security-windows-7-and-windows-server-2008-r2-application-quality-cookbook"></a>Seguridad (Guía de calidad de la aplicación Windows 7 y Windows Server 2008 R2)

A partir de Windows Internet Explorer 7, Windows Internet Explorer se ejecuta en un contexto de seguridad denominado *modo protegido* cuando los usuarios lo ejecutan en el sistema operativo Windows Vista o en una versión posterior. Este modo ejecuta Internet Explorer en una configuración con menos privilegios que una aplicación de usuario estándar, por lo que determinada funcionalidad es limitada, en especial los controles ActiveX y determinados tipos de complementos. Para obtener más información acerca del modo protegido en Internet Explorer y su impacto en la compatibilidad, vea [Descripción y funcionamiento en modo protegido de Internet Explorer](/previous-versions/windows/internet-explorer/ie-developer/) en MSDN Library.

De forma predeterminada, Windows Internet Explorer 8 también habilita la prevención de ejecución de datos (DEP), que ayuda a las aplicaciones a evitar la ejecución de código arbitrario en ataques en línea. Sin embargo, es posible que algunos complementos no utilicen esta característica de seguridad (por ejemplo, los complementos que no están diseñados para ejecutar solo el código que se encuentra en memoria que se ha marcado específicamente como ejecutable, como las aplicaciones compiladas con una versión anterior del marco de trabajo de la biblioteca de plantillas ActiveX (ATL)).

Internet Explorer 8 también protege a los usuarios frente a posibles vulnerabilidades de seguridad que usan scripts. Por ejemplo, no se puede navegar desde una dirección URL de una zona de menos confianza a una dirección URL en una zona más confiable excepto a través de la interacción explícita del usuario. Tampoco puede ocultar ciertos elementos de la interfaz de usuario del explorador (como la barra de direcciones) en una zona que no es de confianza (Internet).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Actualizaciones de diseño que afectan a la compatibilidad entre exploradores](design-updates-that-impact-compatibility-between-browsers.md)
</dt> </dl>

 

 
