---
title: Usar máscaras con el control Reproductor de Windows Media control
description: Usar máscaras con el control Reproductor de Windows Media control
ms.assetid: 0381e0e4-c686-4ab4-b947-b883b6f4e06e
keywords:
- Reproductor de Windows Media, insertar ActiveX control
- Reproductor de Windows Media modelo de objetos, insertar ActiveX control
- object model,embedding ActiveX control
- Reproductor de Windows Media Mobile,embedding ActiveX control
- Reproductor de Windows Media ActiveX control, inserción
- Reproductor de Windows Media Control de ActiveX móvil, inserción
- ActiveX control, inserción
- Reproductor de Windows Media,C++
- Reproductor de Windows Media modelo de objetos, C++
- object model,C++
- Reproductor de Windows Media Mobile,C++
- Reproductor de Windows Media ActiveX control, C++
- Reproductor de Windows Media Control de ActiveX móvil,C++
- ActiveX control, C++
- Inserción de programas de C++
- inserción, programas de C++
- Reproductor de Windows Media ActiveX control, máscaras
- Reproductor de Windows Media Control de ActiveX móviles, máscaras
- ActiveX control, máscaras
- máscaras, insertar ActiveX control
- Reproductor de Windows Media máscaras, insertar ActiveX control
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3714a8be9e471541d008fcb76a4b0398dba2162b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476163"
---
# <a name="using-skins-with-the-windows-media-player-control"></a>Usar máscaras con el control Reproductor de Windows Media control

Al insertar el control Reproductor de Windows Media en un programa de C++, puede personalizar la interfaz de usuario (UI) del reproductor aplicando un archivo de definición de máscara. Un archivo de definición de máscara es un documento basado en XML que especifica el diseño de componentes de interfaz de usuario estándar y personalizables, así como los gráficos adjuntos. Con Microsoft JScript, puede especificar el comportamiento de estos componentes y manipular el control Reproductor de Windows Media sin la sobrecarga de la sintaxis de C++ y COM.

Las máscaras proporcionan una manera sencilla de mantener el código de la interfaz de usuario y el código del programa principal separados para que se puedan mantener y desarrollar de forma independiente. También puede reutilizar máscaras diseñadas originalmente para que las use el reproductor independiente en modo de máscara. El código de máscara que diseñe específicamente para los programas de C++ puede interactuar con los programas a través de un objeto que admite scripts que el programa puede proporcionar.

Para habilitar el modo de máscara para el control Reproductor de Windows Media, el programa debe implementar la **interfaz IWMPRemoteMediaServices.** Aunque puede usar máscaras con el control y el control remoto al mismo tiempo, puede usar esta interfaz para habilitar cualquiera de las características sin habilitar la otra. Para deshabilitar la comunicación remota, simplemente pase un valor de "Local" como parámetro out del método **GetServiceType** y devuelva un HRESULT de E NOTIMPL desde el \_ **método GetApplicationName.**

Para cambiar el control Reproductor de Windows Media al modo de máscara, llame al método **IWMPPlayer::p ut \_ uiMode** y pase un valor de "custom". Especifique la ruta de acceso y el nombre del archivo de definición de máscara que se va a usar devolviendo desde el método **IWMPRemoteMediaServices::GetCustomUIMode.**

Si desea proporcionar un objeto que permite scripts para la comunicación entre la máscara y el programa, pase un nombre y un puntero a un puntero **IDispatch** como los dos parámetros de salida del método **IWMPRemoteMediaServices::GetScriptableObject.** A continuación, la máscara puede realizar llamadas al objeto que puede incluir scripts mediante el nombre especificado como si fuera un atributo global similar al atributo global **del** reproductor.

Una máscara aplicada a un control Reproductor de Windows Media remoto puede acceder al objeto **PlayerApplication** mediante otro atributo global denominado **playerApplication**. Dado que las máscaras no pueden acceder a la propiedad **Player.playerApplication,** debe usar este atributo global cuando desee que el código de máscara administre el acoplamiento y desacoplar.

## <a name="samples"></a>Ejemplos

El Reproductor de Windows Media de instalación del SDK de Reproductor de Windows Media instala un ejemplo que muestra cómo aplicar una máscara al control Reproductor de Windows Media. Consulte el ejemplo RemoteSkin para obtener más información.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Muestras**](samples.md)
</dt> <dt>

[**Usar el control Reproductor de Windows Media en un programa de C++**](using-the-windows-media-player-control-in-a-c---program.md)
</dt> </dl>

 

 




