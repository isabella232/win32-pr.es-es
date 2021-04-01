---
title: Certifique su aplicación de escritorio
description: Siga estos pasos para obtener la certificación de su aplicación de escritorio para Windows 7, Windows 8, Windows 8.1 y Windows 10. Si quiere convertir la aplicación de escritorio para que sea compatible con el Plataforma universal de Windows y la tienda Windows, usará el puente de escritorio de Windows, en cuyo caso debe seguir los pasos de la guía de puente de Desktop para obtener información sobre los pasos de certificación. Si va a desarrollar y certificar una aplicación para UWP desde el principio, consulte la guía de certificación de aplicaciones de Windows en UWP para obtener información sobre la certificación.
ms.assetid: d77d9f1c-1738-4f44-a351-1985ffc21707
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a52eb0f1040c438cb61f4729923c8928116447e8
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/09/2020
ms.locfileid: "103797068"
---
# <a name="certify-your-desktop-application"></a>Certifique su aplicación de escritorio

> [!IMPORTANT]
> La certificación para las aplicaciones de escritorio de Win32 está en [desuso](https://techcommunity.microsoft.com/t5/windows-hardware-certification/win32-logo-certification-deprecation/ba-p/364920). En su lugar, [envíe los archivos aquí](https://www.microsoft.com/wdsi/filesubmission/).

Siga estos pasos para obtener la certificación de su aplicación de escritorio para Windows 7, Windows 8, Windows 8.1 y Windows 10.

Si quiere convertir la aplicación de escritorio para que sea compatible con el Plataforma universal de Windows y la tienda Windows, usará el [puente de escritorio de Windows](https://developer.microsoft.com/windows/bridges/desktop), en cuyo caso debe seguir los pasos de la guía de puente de [Desktop](/windows/uwp/porting/desktop-to-uwp-root) para obtener información sobre los pasos de certificación.

Si va a desarrollar y certificar una aplicación para UWP desde el principio, consulte la [Guía de certificación de aplicaciones de Windows en UWP](/windows/uwp/debug-test-perf/windows-app-certification-kit) para obtener información sobre la certificación.

## <a name="step-1-prepare-for-certification"></a>Paso 1: preparación para la certificación



| Tema                                                                                       | Descripción                                                                                    |
|---------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [¿Cuáles son las ventajas?](what-are-the-benefits-.md)<br/>                             | La certificación de su aplicación de escritorio proporciona varias ventajas a usted y a sus clientes.              |
| [Lea los requisitos](certification-requirements-for-windows-desktop-apps.md)<br/> | Revise los requisitos técnicos y las calificaciones de elegibilidad que una aplicación de escritorio debe cumplir. |



 

## <a name="step-2-test-your-app-with-the-windows-app-certification-kit"></a>Paso 2: probar la aplicación con el kit de certificación de aplicaciones de Windows



| Tema                                                          | Descripción                                                                                                                                                                           |
|----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Obtener el kit](https://developer.microsoft.com/windows/downloads/app-certification-kit/) | Para certificar la aplicación, tiene que instalar y ejecutar el kit de certificación de aplicaciones de Windows (incluido en el Windows SDK).                                                                     |
| [Uso del kit](using-the-windows-app-certification-kit.md)   | Antes de enviar la aplicación, debe probarla para su preparación. También puede descargar una copia de las notas del [producto de certificación](https://www.microsoft.com/download/details.aspx?id=27414)de la aplicación. |
| [Revisar los detalles de la prueba](windows-app-certification-kit-tests.md) | Obtenga la lista de las pruebas que la aplicación debe pasar para que sea apta para la compatibilidad con el sistema operativo Windows más reciente.                                                               |



 

Nota: los controladores de filtro también deben pasar el [Kit de certificación de hardware](https://download.microsoft.com/download/1/8/B/18BC088A-537D-4386-9334-687747A602E6/hlk/hlksetup.exe). (Consulte [requisitos de certificación para aplicaciones de escritorio de Windows, sección 6,2](certification-requirements-for-windows-desktop-apps.md)).

## <a name="step-3-use-the-windows-certification-dashboard"></a>Paso 3: uso del panel de certificación de Windows

Para enviar la aplicación para la certificación, debe iniciar sesión o registrar una cuenta de empresa en el [Panel de certificación de Windows](/previous-versions/hh833792(v=msdn.10)). Una vez hecho, no solo podrá obtener la certificación de la aplicación, sino que también tendrá acceso a las herramientas para revisar y administrar la aplicación en todas las fases del proceso.



| Tema                                                                                                                   | Descripción                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [Configuración de la cuenta](/windows-hardware/drivers/dashboard/)                 | Si su empresa no está registrada, debe registrarla a través del panel de certificación de Windows.                                        |
| [Obtención de un certificado de firma de código](/windows-hardware/drivers/dashboard/)      | Antes de poder establecer una cuenta del panel de certificación de Windows, debe obtener un certificado de firma de código para proteger la información digital. |
| [Probar localmente y cargar los resultados](/windows-hardware/drivers/dashboard/) | Después de ejecutar las pruebas del kit de certificación de aplicaciones de Windows, cargue los resultados en el panel de certificación de Windows.                                 |
| [Administrar el envío](/windows-hardware/drivers/dashboard/)              | Después de enviar la aplicación para la certificación, puede revisar el envío a través del panel de certificación de Windows.                           |



 

## <a name="step-4-promote-your-desktop-app"></a>Paso 4: promoción de la aplicación de escritorio



| Tema                                                                      | Descripción                                                                                                               |
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [Comprobar la compatibilidad de aplicaciones](/windows/compatibility/windows-8-1-introduction) | Si va a compilar una aplicación para Windows 8.1, investigue los problemas de compatibilidad.                                           |
| [Usar el logotipo con la aplicación](https://techcommunity.microsoft.com/t5/windows-hardware-certification/bg-p/WindowsHardwareCertification)                  | Mostrar el logotipo en el embalaje y en los anuncios y otros materiales promocionales de acuerdo con las instrucciones. Solo para Windows 7. |



 

## <a name="see-also"></a>Consulte también:

[Foro de compatibilidad de aplicaciones](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowscompatibility): encuentre soporte técnico de la comunidad sobre compatibilidad y certificación del logotipo.

[Blog de Windows SDK](https://blogs.msdn.com/b/winsdk/archive/tags/certification/): Busque sugerencias y noticias relacionadas con la certificación de aplicaciones.

[Foro de Windows Server]( https://social.technet.microsoft.com/Forums/windowsserver/home?forum=WSAppCompat): visite el foro de certificación para obtener respuestas.

[Guía de compatibilidad](/windows/desktop/w8cookbook/windows-8-and-windows-server-8-compatibility-cookbook-portal): Obtenga información sobre las novedades o los cambios en la versión más reciente de Windows.

 

