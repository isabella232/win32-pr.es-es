---
title: Obtención de la biblioteca DRM requerida
description: Obtención de la biblioteca DRM requerida
ms.assetid: 7bd13b77-439e-40cf-99e8-b359247da74d
keywords:
- Windows SDK de formato multimedia, obtención de las bibliotecas DRM necesarias
- Formato de sistemas avanzados (ASF), obtener las bibliotecas DRM necesarias
- ASF (formato de sistemas avanzados), obtención de las bibliotecas DRM necesarias
- administración de derechos digitales (DRM), obtención de las bibliotecas necesarias
- DRM (administración de derechos digitales), obtención de las bibliotecas necesarias
- administración de derechos digitales (DRM), información de compilación
- DRM (administración de derechos digitales), información de compilación
- administración de derechos digitales (DRM),información de depuración
- DRM (administración de derechos digitales), información de depuración
- depuración de DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20e459423b4a7b9a5bebf03727210951544797519c81886ae9fa792fa8b73be1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119707435"
---
# <a name="obtaining-the-required-drm-library"></a>Obtención de la biblioteca DRM requerida

Para crear o reproducir archivos multimedia digitales protegidos con DRM, la aplicación debe vincularse a una biblioteca estática proporcionada en formato binario por Microsoft. Esta biblioteca a veces se denomina biblioteca de código auxiliar o "stublib" y identifica de forma única la aplicación.

En esta documentación, la biblioteca DRM se conoce como "WMStubDRM.lib". El nombre de la biblioteca que recibe incluirá un número de identificación. Para obtener esta biblioteca, debe firmar un contrato de licencia con Microsoft. Los términos del contrato pueden diferir en función de si solicita una licencia de evaluación o una licencia de producción. Para obtener más información sobre el proceso de licencia de DRM, vea el Windows de licencias multimedia en el sitio [web de Microsoft](https://www.microsoft.com/licensing/default).

La biblioteca que recibe tiene un nivel de seguridad DRM que depende del tipo de contrato de licencia que haya firmado. Una licencia DRM puede impedir que las aplicaciones con componentes DRM por debajo de un nivel de seguridad especificado accedan al contenido del archivo. Este nivel de seguridad no es el mismo que el nivel de individualización de DRM, ni está relacionado con ninguno de los valores numéricos de los niveles de protección de salida (OPL). En la tabla siguiente se muestran ejemplos de niveles de seguridad drm para diferentes reproductores y dispositivos portátiles.



| Nivel de seguridad | Reproductores y dispositivos portátiles                                                                                                                                                                                                                                                                                                   | Ejemplo                                                                                                                                                                                          |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 150            | Dispositivos que no admiten Windows DRM multimedia. La protección DRM se quita cuando el contenido se transfiere a un dispositivo de este tipo.                                                                                                                                                                                                         | Dispositivos que admiten Windows contenido basado en multimedia pero no contenido protegido                                                                                                                       |
| 1,000          | Aplicaciones de reproductor basadas en el SDK de Windows Media Format 9.5 o versiones anteriores que no cumplen los requisitos adicionales para el nivel 2000.Devices basados en Windows Media Portable Device DRM v1.<br/> Dispositivos basados Windows CE 4.2 y versiones posteriores.<br/>                                                                       | Reproductor de Windows Media 6.4, Reproductor de Windows Media 7Portable media devices that support Windows Media Portable Device DRM v1 (Dispositivo multimedia portátil v1).<br/>                                                             |
| 2\.000          | Aplicaciones de reproductor basadas en el SDK de la serie Media Format 9 de Windows o posterior, y que siguen un conjunto más estricto de directrices de protección de contenido que las aplicaciones de nivel 1000.Devices basadas en Windows Media DRM 10 para dispositivos portátiles.<br/> Dispositivos basados Windows DRM multimedia 10 para dispositivos de red.<br/> | Reproductor de Windows Media serie 9 y versiones posterioresPortable media devices that support Windows Media DRM 10 for Portable Devices<br/> Dispositivos portátiles de Media Center basados en Windows Mobile<br/> |



 

## <a name="build-and-debugging-information"></a>Información de compilación y depuración

Al vincular a WMStubDRM.lib, no vincule a wmvcore.lib. El componente DRM no funcionará correctamente si la aplicación se vincula a ambas bibliotecas.

Un punto de interrupción de usuario en el componente DRM impedirá que las versiones de depuración y versión de las aplicaciones accedan al contenido protegido cuando se ejecutan dentro del depurador. Para solucionar problemas de funciones relacionadas con DRM en la aplicación, debe escribir sus propias rutinas de seguimiento que guarden información como valores **HRESULT** en alguna ubicación, como un archivo de registro.

Si intenta ejecutar una versión de lanzamiento de una aplicación en un sistema con una versión de depuración de los bits del SDK instalada (o al revés), se producen errores de montón durante la reproducción del contenido de la versión 7 de DRM. Asegúrese de ejecutar aplicaciones de depuración a través de bits del SDK de depuración y liberar aplicaciones a través de bits de versión. Se producirá el mismo problema si ejecuta una versión de depuración del SDK con un componente DRM individualizado (que siempre es una compilación de versión).

**Notas** DRM no es compatible con la versión basada en x64 de este SDK.

Los archivos WMStubDRM.lib asociados al SDK de Windows Media Format 9.5 solo se pueden usar con los componentes de Microsoft Visual Studio .NET 2003. Si usa una versión anterior de la biblioteca de código auxiliar, no hay nuevas restricciones para su uso.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Habilitación de la compatibilidad con DRM**](enabling-drm-support.md)
</dt> </dl>

 

 





