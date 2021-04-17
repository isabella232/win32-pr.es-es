---
title: Habilitar el registro
description: Habilitar el registro
ms.assetid: 50fc1d71-b650-4ba5-a6e1-631c0b9fe8ad
keywords:
- Administrador de dispositivos de Windows Media, registro
- Administrador de dispositivos, registro
- aplicaciones de escritorio, registro
- proveedores de servicios, registro
- Guía de programación, registro
- logging
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6e95be13e93a5a58bb728d5600c6fdea9801ec2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695273"
---
# <a name="enabling-logging"></a>Habilitar el registro

Windows Media Administrador de dispositivos proporciona un objeto de registro que puede guardar información en un archivo de texto en tiempo de ejecución. Los desarrolladores de aplicaciones y proveedores de servicios pueden utilizar este objeto para almacenar los mensajes en un archivo de registro mientras se ejecuta su aplicación o proveedor de servicios. Este objeto es especialmente útil cuando se administran archivos protegidos con DRM, ya que Windows Media Administrador de dispositivos no le permitirá asociar un depurador a un proceso que controle archivos protegidos con DRM.

El registrador es un objeto COM con el identificador de clase CLSID \_ WMDMLogger que expone una interfaz, [**IWMDMLogger**](/windows/desktop/api/wmdmlog/nn-wmdmlog-iwmdmlogger). Los componentes no necesitan un certificado para usar el objeto de registro.

De forma predeterminada, Windows Media Administrador de dispositivos mantiene un archivo de registro, independientemente de si una aplicación usa **IWMDMLogger**. Este archivo de registro es un archivo de texto simple y cada entrada incluye una entrada precedida por una marca de tiempo con el formato AAAAMMDDHHMMSS, con hora local de 24 horas. Windows Media Administrador de dispositivos registra todas las llamadas API, junto con las entradas que agregue llamando a mensajes **IWMDMLogger** . Todas las entradas del archivo de registro se anexan al archivo hasta que se llama a [**RESET**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-reset) , o el archivo supera su tamaño máximo. El archivo se cierra automáticamente después de cada operación de registro. El mismo archivo de registro se utiliza para entradas de la aplicación y entradas del sistema.

En los pasos siguientes se muestra cómo usar el objeto de registro:

1.  Incluya wmdmlog. h en el proyecto.
2.  Cree un objeto de registro llamando a **CoCreateInstance**(CLSID \_ WMDMLogger) y solicite la interfaz **IWMDMLogger** . Asigne el puntero de interfaz a una variable global.
3.  Compruebe que el registro está habilitado mediante una llamada a [**IWMDMLogger:: IsEnabled**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-isenabled); Si no es así, habilítelo llamando a [**IWMDMLogger:: enable**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-enable).
4.  Especifique un nombre y un tamaño de archivo de registro personalizados. Esto se hace mediante una llamada a [**IWMDMLogger:: SetLogFileName**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-setlogfilename) y [**IWMDMLogger:: SetSizeParams**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-setsizeparams).
5.  En los puntos del código en los que desea crear una entrada en el registro, llame a [**IWMDMLogger:: LogDword**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-logdword) para registrar cadenas que contengan variables (este método es similar a **wsprintf** en la forma en que le permite dar formato a una cadena que contiene un valor de variable), o llamar a [**IWMDMLogger:: LogString**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-logstring) para registrar cadenas de constantes.

Para ver un ejemplo de código, vea las páginas de referencia de los métodos de [**IWMDMLogger**](/windows/desktop/api/wmdmlog/nn-wmdmlog-iwmdmlogger).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Tareas comunes a las aplicaciones y proveedores de servicios**](tasks-common-to-applications-and-service-providers.md)
</dt> </dl>

 

 




