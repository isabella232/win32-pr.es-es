---
title: Obtención de la biblioteca DRM necesaria
description: Obtención de la biblioteca DRM necesaria
ms.assetid: 7bd13b77-439e-40cf-99e8-b359247da74d
keywords:
- SDK de Windows Media Format, obtención de las bibliotecas DRM necesarias
- Advanced Systems Format (ASF), obtención de las bibliotecas DRM necesarias
- ASF (formato de sistemas avanzados), obtención de las bibliotecas DRM necesarias
- Administración de derechos digitales (DRM), obtención de las bibliotecas necesarias
- DRM (administración de derechos digitales), obtención de las bibliotecas necesarias
- Administración de derechos digitales (DRM), información de compilación
- DRM (administración de derechos digitales), información de compilación
- Administración de derechos digitales (DRM), información de depuración
- DRM (administración de derechos digitales), información de depuración
- depuración de DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f5c124c1e7edf0bba736b9dd392e852aac97e96
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/09/2020
ms.locfileid: "104421547"
---
# <a name="obtaining-the-required-drm-library"></a>Obtención de la biblioteca DRM necesaria

Para crear o reproducir archivos multimedia digitales protegidos con DRM, la aplicación debe vincularse a una biblioteca estática que Microsoft proporcione en formato binario. Esta biblioteca se denomina a veces biblioteca de código auxiliar o "stublib" e identifica la aplicación de forma única.

En esta documentación, la biblioteca DRM se conoce como "WMStubDRM. lib". El nombre de la biblioteca que reciba incluirá un número de identificación. Para obtener esta biblioteca, debe firmar un contrato de licencia con Microsoft. Los términos del acuerdo pueden diferir en función de si solicita una licencia de evaluación o una licencia de producción. Para obtener más información sobre el proceso de licencias de DRM, vea el formulario de licencias de Windows Media en el [sitio web de Microsoft](https://www.microsoft.com/licensing/default).

La biblioteca que recibe tiene un nivel de seguridad DRM que depende del tipo de contrato de licencia que especifique en. Una licencia DRM puede restringir a las aplicaciones con componentes DRM por debajo de un nivel de seguridad especificado el acceso al contenido del archivo. Este nivel de seguridad no es el mismo que el nivel de individualización de DRM ni está relacionado con ninguno de los valores numéricos de los niveles de protección de la salida (OPLs). En la tabla siguiente se muestran ejemplos de niveles de seguridad de DRM para distintos reproductores y dispositivos portátiles.



| Nivel de seguridad | Jugadores y dispositivos portátiles                                                                                                                                                                                                                                                                                                   | Ejemplo                                                                                                                                                                                          |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 150            | Dispositivos que no admiten DRM de Windows Media. La protección DRM se quita cuando el contenido se transfiere a este tipo de dispositivo.                                                                                                                                                                                                         | Dispositivos que admiten contenido basado en Windows Media, pero no contenido protegido                                                                                                                       |
| 1,000          | Aplicaciones de reproductor basadas en el SDK de Windows Media Format 9,5 o una versión anterior que no cumplen los requisitos adicionales para el nivel 2000. dispositivos basados en DRM de dispositivos portátiles de Windows Media v1.<br/> Dispositivos basados en Windows CE 4,2 y versiones posteriores.<br/>                                                                       | Windows Media Player 6,4, Windows Media Player 7Portable dispositivos multimedia compatibles con DRM de dispositivos portátiles de Windows Media v1.<br/>                                                             |
| 2\.000          | Aplicaciones de reproductor basadas en el SDK de Windows Media Format 9 series o posterior, y que siguen un conjunto más estricto de directrices de protección de contenido que las aplicaciones en el nivel 1000. dispositivos basados en Windows Media DRM 10 para dispositivos portátiles.<br/> Dispositivos basados en Windows Media DRM 10 para dispositivos de red.<br/> | Windows Media Player 9 series y dispositivos multimedia laterPortable compatibles con Windows Media DRM 10 para dispositivos portátiles<br/> Dispositivos portátiles de Media Center basados en Windows Mobile<br/> |



 

## <a name="build-and-debugging-information"></a>Información de compilación y depuración

Al vincular a WMStubDRM. lib, no vincule a wmvcore. lib. El componente DRM no funcionará correctamente si la aplicación se vincula a ambas bibliotecas.

Un punto de interrupción de usuario en el componente DRM impedirá que las versiones de depuración y lanzamiento de las aplicaciones tengan acceso al contenido protegido cuando se ejecute en el depurador. Para solucionar problemas relacionados con las funciones de DRM en la aplicación, debe escribir sus propias rutinas de seguimiento que guarden información como valores **HRESULT** en alguna ubicación, como un archivo de registro.

Si intenta ejecutar una versión de lanzamiento de una aplicación en un sistema con una versión de depuración de los bits de SDK instalados (o de otra forma), se producirán errores en el montón durante la reproducción del contenido de la versión 7 de DRM. Asegúrese de ejecutar las aplicaciones de depuración sobre los bits del SDK de depuración y de liberar las aplicaciones con bits de versión. El mismo problema se producirá si ejecuta una versión de depuración del SDK con un componente DRM individual (que es siempre una compilación de versión).

**Notas** de DRM no es compatible con la versión basada en x64 de este SDK.

Los archivos WMStubDRM. lib asociados al SDK de Windows Media Format 9,5 solo se pueden usar con los componentes de Microsoft Visual Studio .NET 2003. Si usa una versión anterior de la biblioteca de código auxiliar, no hay restricciones nuevas para su uso.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Habilitar la compatibilidad con DRM**](enabling-drm-support.md)
</dt> </dl>

 

 





