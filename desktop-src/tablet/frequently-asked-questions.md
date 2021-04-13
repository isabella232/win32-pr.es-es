---
description: A continuación se indican las preguntas más frecuentes (p + f) sobre el desarrollo de los componentes de la plataforma de Tablet PC instalados por el SDK de Windows Vista.
ms.assetid: eb349493-a2b2-4b58-bcbc-ee09953c8dc8
title: Preguntas más frecuentes (Tablet PC)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8722c00fa5aaf2b43494484fc015fa8b3e4c7826
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/18/2020
ms.locfileid: "104421707"
---
# <a name="frequently-asked-questions-about-developing-for-the-tablet-pc-platform"></a>Preguntas más frecuentes sobre el desarrollo de la plataforma de Tablet PC

A continuación se indican las preguntas más frecuentes (p + f) sobre el desarrollo de los componentes de la plataforma de Tablet PC instalados por el SDK de Windows Vista.

## <a name="q-can-i-use-the-ink-apis-or-controls-in-a-web-page"></a>Q. ¿Puedo usar los controles o las API de entrada de lápiz en una página web?

A. Sí. La biblioteca administrada de Tablet PC es compatible con entornos de confianza parcial, es decir, la ejecución de ensamblados administrados desde páginas Web.

También se admite la implementación del explorador de aplicaciones que usan Windows Presentation Foundation.

## <a name="q-do-i-need-a-tablet-pc-to-develop-tablet-pc-applications"></a>Q. ¿Necesito un Tablet PC para desarrollar aplicaciones de Tablet PC?

A. No, los componentes de la plataforma de Tablet PC instalados por el Windows SDK incluyen las extensiones y utilidades necesarias para desarrollar software para Tablet PC en un equipo de escritorio o portátil. Puede usar un mouse o una tableta externa para entradas manuscritas y manuscritas.

Los componentes de la plataforma de Tablet PC instalados por el Windows SDK se pueden instalar en Windows XP Professional o Windows Server 2003, pero hay menos funcionalidad disponible para las aplicaciones. En estas plataformas, la aplicación puede recopilar entradas manuscritas con los objetos [**InkCollector**](inkcollector-class.md) y [**InkOverlay**](inkoverlay-class.md) y se puede probar y depurar.

Además, los controles [InkEdit](inkedit-control-reference.md) y [InkPicture](inkpicture-control-reference.md) solo pueden recopilar entradas manuscritas en estos sistemas operativos si los componentes de la plataforma de Tablet PC se han instalado desde el Windows SDK (o una versión anterior del kit de desarrollo de Tablet PC). no recopilan entradas manuscritas en aplicaciones que se redistribuyen a equipos que no son de Tablet PC sin los componentes de la plataforma instalados.

## <a name="q-do-i-need-to-run-a-special-version-of-windows-to-do-handwriting-recognition"></a>Q. ¿Es necesario ejecutar una versión especial de Windows para realizar el reconocimiento de escritura a mano?

A. No. Aunque solo Windows XP Tablet PC Edition y ciertas versiones de Windows Vista incluyen reconocedores de escritura a mano, puede descargar el [paquete de reconocimiento de Windows XP Tablet PC edition 2005]( https://www.microsoft.com/downloads/details.aspx?FamilyId=080184DD-5E92-4464-B907-10762E9F918B&amp;displaylang=en) e instalarlo en Windows XP Professional o windows Server 2003 solo con fines de desarrollo. No puede redistribuir los reconocedores con su aplicación.

## <a name="q-what-is-the-difference-between-windows-vista-and-tablet-pc-technology"></a>Q. ¿Cuál es la diferencia entre Windows Vista y la tecnología de Tablet PC?

A. Los Tablet PC ejecutan el sistema operativo Windows Vista, que incluye toda la funcionalidad de Windows Vista, además de características adicionales específicas de Tablet PC. Estas características de tecnología de Tablet PC permiten a los usuarios ejecutar aplicaciones Windows y Windows mediante el uso de un lápiz, anotar documentos y crear documentos manuscritos mediante la entrada de lápiz digital. La tecnología de Tablet PC está disponible en la mayoría de las versiones de Windows Vista y, si el hardware de Tablet PC está disponible en un equipo, las características funcionan simplemente.

En las versiones anteriores de los sistemas operativos Windows que no admiten de forma nativa la tinta, puede redistribuir y usar los controles de tinta de Tablet PC para ver la tinta dibujada en Tablet PC.

## <a name="q-what-is-the-difference-between-windows-xp-tablet-pc-edition-and-windows-xp-tablet-pc-edition-2005"></a>Q. ¿Cuál es la diferencia entre Windows XP Tablet PC Edition y Windows XP Tablet PC Edition 2005?

A. Windows XP Tablet PC Edition 2005 es una versión actualizada de Windows XP Tablet PC Edition.

## <a name="q-how-do-i-modify-my-application-to-run-on-a-tablet-pc"></a>Q. ¿Cómo modificar la aplicación para que se ejecute en un Tablet PC?

A. Las aplicaciones de Microsoft Windows que se ejecutan en un equipo portátil o de escritorio con Windows XP con hardware comparable se pueden ejecutar en un Tablet PC sin modificaciones.

## <a name="q-i-understand-that-i-dont-need-to-make-any-changes-to-my-application-but-it-is-difficult-to-use-it-with-a-pen-and-speech-what-can-i-do-to-optimize-my-application-for-a-tablet-pc"></a>Q. Entiendo que no es necesario realizar ningún cambio en la aplicación, pero es difícil usarlo con un lápiz y voz. ¿Qué se puede hacer para optimizar la aplicación para Tablet PC?

A. Los controles de entrada y API de los componentes de la plataforma de Tablet PC se pueden usar para crear interfaces de usuario que se adapten mejor a la entrada de lápiz y escritura a mano. Para obtener más información acerca de cómo puede mejorar la aplicación, consulte [directrices para la experiencia del usuario de PC móvil para desarrolladores](/previous-versions//dd356056(v=vs.85)).

## <a name="q-what-programming-languages-does-the-tablet-support"></a>Q. ¿Qué lenguajes de programación admite la tableta?

A. La tecnología de Tablet PC de Windows Vista admite bibliotecas COM (C++) y administradas (el conjunto de lenguajes .NET de Visual Studio).

La tecnología de Tablet PC también admite Windows Presentation Foundation (WPF).

## <a name="q-do-i-have-sample-code-that-demonstrates-tablet-platform-capabilities"></a>Q. ¿Tengo código de ejemplo que muestra las capacidades de la plataforma de tableta?

A. Sí, el código de ejemplo para COM y los idiomas administrados seleccionados se incluye en los componentes de la plataforma de Tablet PC instalados por el SDK de la plataforma Windows.

Para ver las aplicaciones de ejemplo disponibles, consulte:

- [Ejemplos de PC móvil y Tablet PC](mobile-pc-and-tablet-pc-samples.md)
- [Ejemplos de tinta digital, Windows Presentation Foundation (WPF)](/previous-versions/dotnet/netframework-3.0/aa972145(v=vs.85))
- <systemdrive>: \\ Archivos de programa \\ Microsoft SDK \\ Windows \\ v 6.0 \\ Samples \\ TabletPC

## <a name="q-whats-the-base-level-of-tablet-hardware-that-i-should-develop-for"></a>Q. ¿Cuál es el nivel básico de hardware de Tablet PC para el que debo desarrollar?

A. En general, debe diseñar un sistema de disponibilidad heredado compatible con Windows Vista.

## <a name="q-what-user-interface-guidelines-can-you-provide-for-tablet-applications"></a>Q. ¿Qué instrucciones de interfaz de usuario puede proporcionar para las aplicaciones de Tablet PC?

A. Los problemas de la orientación del menú desplegable al filtro Parallax de pantalla/digitalizador se describen en la sección [sobre la experiencia del usuario de PC móvil para desarrolladores](/previous-versions//dd356056(v=vs.85)) en la sección PC móvil del Windows SDK.

## <a name="q-do-you-include-system-level-handwriting-gestures-for-commonly-used-keystrokes-can-i-create-my-own-gestures-for-use-when-an-application-is-running-or-has-focus"></a>Q. ¿Se incluyen los gestos de escritura a mano de nivel de sistema para las pulsaciones de teclas más utilizadas? ¿Puedo crear mis propios gestos para usarlos cuando una aplicación se está ejecutando o tiene el foco?

A. Sí, se incluye un conjunto de gestos para los eventos del mouse. Además, puede crear gestos para usarlos en la aplicación. Para obtener más información acerca de los gestos, vea [uso de gestos](using-gestures.md).

## <a name="q-how-can-i-determine-whether-my-application-is-running-on-a-tablet"></a>Q. ¿Cómo se puede determinar si la aplicación se está ejecutando en una tableta?

A. Use el GetSystemMetricsAPI de Windows y pase SM \_ TABLETPC como valor del índice. SM \_ TABLETPC se define en Winuser. h. El valor de SM \_ TABLETPC es 86.

Para el desarrollo web, debe leer la \_ variable de entorno User Agent \_ String. Puede tener acceso a esta colección request. ServerVariables.

Para obtener más información sobre cómo usar GetSystemMetrics en Tablet PC con Windows Vista o Windows XP Tablet PC Edition, consulte [determinar si un equipo es un Tablet PC](determining-whether-a-pc-is-a-tablet-pc.md).

## <a name="q-how-can-i-determine-whether-tablet-platform-components-are-available"></a>Q. ¿Cómo se puede determinar si los componentes de la plataforma de tableta están disponibles?

A. Ciertas partes de la plataforma de Tablet PC se pueden instalar en versiones que no son de Tablet PC de los sistemas operativos Windows XP Professional, Windows Server 2003 y Windows 2000.

La manera adecuada de determinar si un componente de la API está instalada es intentar crear una instancia de un objeto o un control y comprobar que existe antes de intentar usarlo.

Por ejemplo, para determinar si el objeto [**InkCollector**](inkcollector-class.md) está disponible, intente crearlo mediante [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).

```C++
IInkCollector* pIInkCollector = NULL;
HRESULT hr = CoCreateInstance(CLSID_InkCollector,
 NULL, CLSCTX_INPROC_SERVER, 
 IID_IInkCollector,
 (void **)&pIInkCollector);
if (SUCCEEDED(hr)) 
{ 
  /* InkCollector is usable. */ 
} else 
{
  /* InkCollector unavailable. */
}
```

## <a name="q-how-do-i-run-the-tablet-input-service-on-server-skus"></a>Q. Cómo ejecutar el servicio de entrada de Tablet PC en las SKU de servidor

A. TabletInputService está diseñado para no ejecutarse automáticamente en las SKU de servidor cuando se instala el paquete de cliente. El paquete de cliente instala todos los componentes de la plataforma para que cualquiera de las aplicaciones cliente de Tablet PC pueda ejecutarse también en un servidor. El servicio de entrada de Tablet PC escucha la notificación de PnP en la que está conectado un digitalizador externo. Para habilitar el servicio de entrada de Tablet PC en un servidor, use la utilidad de configuración del sistema.

En el menú **Inicio** , seleccione **Ejecutar**. Escriba "msconfig" y presione Entrar. Seleccione la pestaña **servicios** , busque los servicios denominados "servicio de entrada HID", active la casilla situada junto a él y, a continuación, haga clic en **aplicar**. Cierre la utilidad.

## <a name="q-more-faqs-and-other-resources"></a>Q. Más preguntas más frecuentes y otros recursos

- [Centro para desarrolladores de Microsoft](https://developer.microsoft.com)
- [Referencia básica de Tablet PC](./core-reference---tablet-pc-com-library.md)