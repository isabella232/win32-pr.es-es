---
title: Para agregar datos de script al encabezado
description: Para agregar datos de script al encabezado
ms.assetid: 25f63d9e-c81a-4098-81d4-e848659a60e5
keywords:
- Windows SDK de formato multimedia, agregar datos de script a encabezados
- Formato de sistemas avanzados (ASF), agregar datos de script a encabezados
- ASF (formato de sistemas avanzados), agregar datos de script a encabezados
- scripts, agregar datos a encabezados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8052d8a5ae04b0ea821d716bf1931352c591f892
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359903"
---
# <a name="to-add-script-data-to-the-header"></a>Para agregar datos de script al encabezado

Puede incluir comandos de script en el encabezado de un archivo ASF. Para escribir comandos de script en el encabezado en el momento de la codificación, realice los pasos siguientes. Realice estos pasos antes de llamar a [**IWMWriter::BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting).

1.  Obtenga un puntero a la **interfaz IWMHeaderInfo** llamando a **IWMWriter::QueryInterface**.
2.  Agregue cada comando de script deseado llamando [**a IWMHeaderInfo::AddScript**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-addscript). Cada llamada toma las dos cadenas por separado y el tiempo de presentación que se usará para el comando como parámetros.

Cuando una aplicación lee el archivo, deberá recuperar todos los comandos de script. Para buscar todos los comandos de script en el encabezado de un archivo, realice los pasos siguientes. Esto debe hacerse antes de iniciar la reproducción.

1.  Obtenga un puntero a la **interfaz IWMHeaderInfo** del objeto de lector (u objeto de lector sincrónico) llamando al método **QueryInterface** de otra interfaz del objeto .
2.  Obtenga el número total de scripts del encabezado llamando a [**IWMHeaderInfo::GetScriptCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getscriptcount).
3.  Recorrer en bucle todos los scripts del encabezado de uno en uno mediante llamadas a [**IWMHeaderInfo::GetScript**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getscript).
4.  Cree una lista de los tiempos de presentación para que la aplicación pueda reaccionar a los comandos en el momento adecuado.

> [!Note]  
> Cuando se usa DRM para cifrar un archivo, ningún comando de script puede tener un tiempo de presentación de 0.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IWMHeaderInfo (interfaz)**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)
</dt> <dt>

[**IWMWriter (Interfaz)**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter)
</dt> <dt>

[**Uso de comandos de script**](using-script-commands.md)
</dt> </dl>

 

 




