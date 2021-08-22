---
title: Habilitar el registro
description: Habilitar el registro
ms.assetid: 50fc1d71-b650-4ba5-a6e1-631c0b9fe8ad
keywords:
- Windows Registro Administrador de dispositivos multimedia
- Administrador de dispositivos, registro
- aplicaciones de escritorio, registro
- proveedores de servicios, registro
- guía de programación, registro
- logging
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ff937b2a3abd16f7319c3abb73a3a2159350049fff8c89d343cc5545f8a21ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118585123"
---
# <a name="enabling-logging"></a>Habilitar el registro

Windows El Administrador de dispositivos proporciona un objeto de registro que puede guardar información en un archivo de texto en tiempo de ejecución. Los desarrolladores de aplicaciones y proveedores de servicios pueden usar este objeto para almacenar mensajes en un archivo de registro mientras se ejecuta su aplicación o proveedor de servicios. Este objeto es especialmente útil al controlar archivos protegidos con DRM, ya que Windows Media Administrador de dispositivos no le permitirá asociar un depurador a un proceso que controle archivos protegidos con DRM.

El registrador es un objeto COM con el identificador de clase CLSID WMDMLogger que expone \_ una interfaz, [**IWMDMLogger**](/windows/desktop/api/wmdmlog/nn-wmdmlog-iwmdmlogger). Los componentes no necesitan un certificado para usar el objeto de registro.

De forma predeterminada, Windows media Administrador de dispositivos mantiene un archivo de registro, independientemente de si una aplicación usa **IWMDMLogger**. Este archivo de registro es un archivo de texto simple y cada entrada incluye una entrada precedida de una marca de tiempo con el formato AAAAMMDDHHMMSS, con una hora local de 24 horas. Windows El Administrador de dispositivos registra todas las llamadas API, junto con las entradas que agregue mediante una llamada **a mensajes IWMDMLogger.** Todas las entradas del archivo de registro se anexan al archivo hasta que se llama a [**Reset**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-reset) o el archivo supera su tamaño máximo. El archivo se cierra automáticamente después de cada operación de registro. El mismo archivo de registro se usa para las entradas de la aplicación y las entradas del sistema.

En los pasos siguientes se muestra cómo usar el objeto de registro:

1.  Incluya wmdmlog.h en el proyecto.
2.  Cree un objeto de registro llamando a **CoCreateInstance**(CLSID WMDMLogger) y solicitando \_ la interfaz **IWMDMLogger.** Asigne el puntero de interfaz a una variable global.
3.  Compruebe que el registro está habilitado llamando a [**IWMDMLogger::IsEnabled**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-isenabled); Si no es así, para habilitarlo, llame a [**IWMDMLogger::Enable**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-enable).
4.  Especifique un nombre y un tamaño de archivo de registro personalizados. Para ello, se [**llama a IWMDMLogger::SetLogFileName**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-setlogfilename) e [**IWMDMLogger::SetSizeParams**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-setsizeparams).
5.  En los puntos del código en los que desea realizar una entrada en el registro, llame a [**IWMDMLogger::LogDword**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-logdword) para registrar cadenas que contengan variables (este método es similar a **wsprintf** en la forma en que permite dar formato a una cadena que contiene un valor de variable) o llame a [**IWMDMLogger::LogString**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-logstring) para registrar cadenas constantes.

Para obtener código de ejemplo, vea las páginas de referencia de los métodos [**de IWMDMLogger**](/windows/desktop/api/wmdmlog/nn-wmdmlog-iwmdmlogger).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Tareas comunes para aplicaciones y proveedores de servicios**](tasks-common-to-applications-and-service-providers.md)
</dt> </dl>

 

 




