---
title: Para agregar datos de script al encabezado
description: Para agregar datos de script al encabezado
ms.assetid: 25f63d9e-c81a-4098-81d4-e848659a60e5
keywords:
- SDK de Windows Media Format, agregar datos de script a encabezados
- Advanced Systems Format (ASF), agregar datos de script a encabezados
- ASF (formato de sistemas avanzados), agregar datos de script a encabezados
- scripts, agregar datos a encabezados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8052d8a5ae04b0ea821d716bf1931352c591f892
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2020
ms.locfileid: "105704921"
---
# <a name="to-add-script-data-to-the-header"></a>Para agregar datos de script al encabezado

Puede incluir comandos de script en el encabezado de un archivo ASF. Para escribir comandos de script en el encabezado en el momento de la codificación, realice los pasos siguientes. Siga estos pasos antes de llamar a [**IWMWriter:: BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting).

1.  Obtenga un puntero a la interfaz **IWMHeaderInfo** llamando a **IWMWriter:: QueryInterface**.
2.  Agregue cada comando de script deseado llamando a [**IWMHeaderInfo:: AddScript**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-addscript). Cada llamada toma las dos cadenas por separado y el tiempo de presentación que se va a usar para el comando como parámetros.

Cuando una aplicación Lea el archivo, tendrá que recuperar todos los comandos de script. Para buscar todos los comandos de script en el encabezado de un archivo, realice los pasos siguientes. Esto debe realizarse antes de iniciar la reproducción.

1.  Obtenga un puntero a la interfaz **IWMHeaderInfo** del objeto lector (o del objeto lector sincrónico) mediante una llamada al método **QueryInterface** de otra interfaz en el objeto.
2.  Obtenga el número total de scripts en el encabezado mediante una llamada a [**IWMHeaderInfo:: GetScriptCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getscriptcount).
3.  Recorra en bucle todos los scripts del encabezado de uno en uno mediante llamadas a [**IWMHeaderInfo:: GetScript**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getscript).
4.  Cree una lista de los tiempos de presentación para que la aplicación pueda reaccionar a los comandos en el momento adecuado.

> [!Note]  
> Al usar DRM para cifrar un archivo, ningún comando de script puede tener un tiempo de presentación de 0.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Interfaz IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)
</dt> <dt>

[**Interfaz IWMWriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter)
</dt> <dt>

[**Usar comandos de script**](using-script-commands.md)
</dt> </dl>

 

 




