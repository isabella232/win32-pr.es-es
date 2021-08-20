---
title: Certificación de la aplicación de escritorio
description: Siga estos pasos para certificar la aplicación de escritorio para Windows 7, Windows 8, Windows 8.1 y Windows 10. Si desea convertir la aplicación de escritorio para que sea compatible con la Plataforma universal de Windows y la Tienda Windows, usará el Windows Puente de dispositivo de escritorio, en cuyo caso debe seguir las instrucciones de Puente de dispositivo de escritorio para los pasos de certificación. Si vas a desarrollar y certificar una aplicación para UWP desde el principio, consulta Guidance for Windows App Certification in UWP (Guía para la certificación de aplicaciones de Windows en UWP) para obtener información sobre la certificación.
ms.assetid: d77d9f1c-1738-4f44-a351-1985ffc21707
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9434b298cbfd3b0979133407273e7631d91faf922687cb59441c614a1fb8704
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118031816"
---
# <a name="certify-your-desktop-application"></a>Certificación de la aplicación de escritorio

> [!IMPORTANT]
> La certificación para aplicaciones de escritorio Win32 está [en desuso.](https://techcommunity.microsoft.com/t5/windows-hardware-certification/win32-logo-certification-deprecation/ba-p/364920) En su lugar, [envíe los archivos aquí.](https://www.microsoft.com/wdsi/filesubmission/)

Siga estos pasos para certificar la aplicación de escritorio para Windows 7, Windows 8, Windows 8.1 y Windows 10.

Si quiere convertir la aplicación de escritorio para que sea compatible con la Plataforma universal de Windows y Windows Store, [](/windows/uwp/porting/desktop-to-uwp-root) usará Windows Puente de dispositivo de escritorio [,](https://developer.microsoft.com/windows/bridges/desktop)en cuyo caso debe seguir las instrucciones de Puente de dispositivo de escritorio para los pasos de certificación.

Si vas a desarrollar y certificar una aplicación para UWP desde el principio, consulta Guidance for Windows App Certification in UWP (Guía para la certificación de aplicaciones en [UWP)](/windows/uwp/debug-test-perf/windows-app-certification-kit) para obtener información sobre la certificación.

## <a name="step-1-prepare-for-certification"></a>Paso 1: Preparación para la certificación



| Tema                                                                                       | Descripción                                                                                    |
|---------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [¿Cuáles son las ventajas?](what-are-the-benefits-.md)<br/>                             | Certificar la aplicación de escritorio proporciona varias ventajas para usted y sus clientes.              |
| [Leer los requisitos](certification-requirements-for-windows-desktop-apps.md)<br/> | Revise los requisitos técnicos y las aptitudes de idoneidad que debe cumplir una aplicación de escritorio. |



 

## <a name="step-2-test-your-app-with-the-windows-app-certification-kit"></a>Paso 2: Probar la aplicación con el kit de certificación Windows aplicaciones



| Tema                                                          | Descripción                                                                                                                                                                           |
|----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Obtener el kit](https://developer.microsoft.com/windows/downloads/app-certification-kit/) | Para certificar la aplicación, debe instalar y ejecutar Windows App Certification Kit (incluido en Windows SDK).                                                                     |
| [Uso del kit](using-the-windows-app-certification-kit.md)   | Para poder enviar la aplicación, debe probarla para obtener preparación. También puede descargar una copia de las white [paper de certificación de la aplicación](https://www.microsoft.com/download/details.aspx?id=27414). |
| [Revisión de los detalles de las pruebas](windows-app-certification-kit-tests.md) | Obtenga la lista de las pruebas que la aplicación debe superar para calificar para la compatibilidad con la versión Windows sistema operativo.                                                               |



 

Nota: Los controladores de filtro también deben pasar el [Kit de certificación de hardware](https://download.microsoft.com/download/1/8/B/18BC088A-537D-4386-9334-687747A602E6/hlk/hlksetup.exe). (Consulte Requisitos de certificación [Windows aplicaciones de escritorio, sección 6.2).](certification-requirements-for-windows-desktop-apps.md)

## <a name="step-3-use-the-windows-certification-dashboard"></a>Paso 3: Uso del panel Windows certificación

Para enviar la aplicación para su certificación, deberá iniciar sesión o registrar una cuenta de empresa en el Windows [de certificación.](/previous-versions/hh833792(v=msdn.10)) Una vez hecho esto, no solo podrá certificar la aplicación, sino que también obtendrá acceso a herramientas para revisar y administrar la aplicación en todas las fases del proceso.



| Tema                                                                                                                   | Descripción                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [Configuración de la cuenta](/windows-hardware/drivers/dashboard/)                 | Si su empresa aún no está registrada, debe registrarla a través del panel Windows certificación.                                        |
| [Obtención de un certificado de firma de código](/windows-hardware/drivers/dashboard/)      | Para poder establecer una cuenta Windows de certificación, debe obtener un certificado de firma de código para proteger la información digital. |
| [Prueba local y carga de los resultados](/windows-hardware/drivers/dashboard/) | Después de ejecutar las pruebas Windows App Certification Kit, cargue los resultados en el panel Windows certificación.                                 |
| [Administración del envío](/windows-hardware/drivers/dashboard/)              | Después de enviar la aplicación para su certificación, puede revisar el envío a través del panel Windows certificación.                           |



 

## <a name="step-4-promote-your-desktop-app"></a>Paso 4: Promoción de la aplicación de escritorio



| Tema                                                                      | Descripción                                                                                                               |
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [Comprobación de la compatibilidad de aplicaciones](/windows/compatibility/windows-8-1-introduction) | Si va a compilar una aplicación para Windows 8.1, investigue los problemas de compatibilidad.                                           |
| [Uso del logotipo con la aplicación](https://techcommunity.microsoft.com/t5/windows-hardware-certification/bg-p/WindowsHardwareCertification)                  | Muestre el logotipo en el empaquetado y en anuncios y otros materiales promocionales según las directrices. Solo Windows 7. |



 

## <a name="see-also"></a>Consulte también:

[Foro de compatibilidad de aplicaciones:](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowscompatibility)busque soporte técnico de la comunidad sobre compatibilidad y certificación de logotipos.

[Windows blog del SDK:](https://blogs.msdn.com/b/winsdk/archive/tags/certification/)busque sugerencias y noticias relacionadas con la certificación de aplicaciones.

[Windows Server:]( https://social.technet.microsoft.com/Forums/windowsserver/home?forum=WSAppCompat)visite el foro de certificación para obtener respuestas.

[Guía de compatibilidad:](/windows/desktop/w8cookbook/windows-8-and-windows-server-8-compatibility-cookbook-portal)obtenga información sobre las novedades o los cambios en la versión más reciente de Windows.

 

