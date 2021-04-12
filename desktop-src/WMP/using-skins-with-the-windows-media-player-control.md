---
title: Usar máscaras con el control Media Player de Windows
description: Usar máscaras con el control Media Player de Windows
ms.assetid: 0381e0e4-c686-4ab4-b947-b883b6f4e06e
keywords:
- Windows Media Player, incrustar el control ActiveX
- Modelo de objetos de Windows Media Player, incrustar el control ActiveX
- modelo de objetos, incrustar el control ActiveX
- Windows Media Player Mobile, incrustar el control ActiveX
- Control ActiveX de Windows Media Player, incrustación
- Control ActiveX móvil de Windows Media Player, incrustación
- Control ActiveX, incrustación
- Windows Media Player, C++
- Modelo de objetos de Windows Media Player, C++
- modelo de objetos, C++
- Windows Media Player Mobile, C++
- Control ActiveX de Windows Media Player, C++
- Control ActiveX móvil de Windows Media Player, C++
- Control ActiveX, C++
- Incrustación de programas de C++
- incrustación, programas de C++
- Control ActiveX de Windows Media Player, máscaras
- Control ActiveX móvil de Windows Media Player, máscaras
- Control ActiveX, máscaras
- máscaras, incrustar el control ActiveX
- Aspectos de Windows Media Player, incrustar el control ActiveX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3714a8be9e471541d008fcb76a4b0398dba2162b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268812"
---
# <a name="using-skins-with-the-windows-media-player-control"></a>Usar máscaras con el control Media Player de Windows

Al incrustar el control Media Player de Windows en un programa de C++, puede personalizar la interfaz de usuario (UI) del reproductor aplicando un archivo de definición de máscara a él. Un archivo de definición de máscara es un documento basado en XML que especifica el diseño de componentes de interfaz de usuario estándar y personalizables y los gráficos que lo acompañan. Con Microsoft JScript, puede especificar el comportamiento de estos componentes y manipular el control de Media Player de Windows sin la sobrecarga de C++ y la sintaxis COM.

Las máscaras proporcionan una manera fácil de mantener el código de la interfaz de usuario y el código de programa principal por separado para que se puedan mantener y desarrollar de manera independiente. También puede reutilizar máscaras diseñadas originalmente para su uso por parte del reproductor independiente en modo de máscara. El código de máscara diseñado específicamente para los programas de C++ puede interactuar con los programas a través de un objeto que puede incluirse en scripts y que el programa puede proporcionar.

Para habilitar el modo de máscara para el control Media Player de Windows, el programa debe implementar la interfaz **IWMPRemoteMediaServices** . Aunque puede usar máscaras con el control y el control remoto al mismo tiempo, puede usar esta interfaz para habilitar cualquiera de las características sin habilitar la otra. Para deshabilitar la comunicación remota, solo tiene que pasar un valor "local" como parámetro out del método **GetServiceType** y devolver un valor HRESULT de E \_ NOTIMPL desde el método **GetApplicationName** .

Para cambiar el control de Media Player de Windows al modo de máscara, llame al método **IWMPPlayer::p UT \_ uiMode** , pasando un valor de "Custom". Especifique la ruta de acceso y el nombre de archivo del archivo de definición de máscara que se va a usar devolviéndolo desde el método **IWMPRemoteMediaServices:: GetCustomUIMode** .

Si desea proporcionar un objeto que admite scripts para la comunicación entre la máscara y el programa, pase un nombre y un puntero a un puntero **IDispatch** como los dos parámetros out del método **IWMPRemoteMediaServices:: GetScriptableObject** . Después, la máscara puede realizar llamadas al objeto que admite scripts mediante el uso del nombre especificado como si fuera un atributo global similar al atributo global del **reproductor** .

Una máscara aplicada a un control de Windows Media Player remoto puede tener acceso al objeto **PlayerApplication** mediante otro atributo global denominado **PlayerApplication**. Dado que las máscaras no pueden tener acceso a la propiedad **Player. playerApplication** , debe usar este atributo global cuando desee que el código de máscara administre el acoplamiento y desacoplamiento.

## <a name="samples"></a>Ejemplos

El paquete de instalación de Windows Media Player SDK instala un ejemplo que muestra cómo aplicar una máscara al control Media Player de Windows. Vea el ejemplo RemoteSkin para obtener más información.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Ejemplos**](samples.md)
</dt> <dt>

[**Usar el control Media Player de Windows en un programa de C++**](using-the-windows-media-player-control-in-a-c---program.md)
</dt> </dl>

 

 




