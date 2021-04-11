---
description: Cargar un archivo de proyecto
ms.assetid: f8d142bd-e51d-4714-893b-8e3d02506891
title: Cargar un archivo de proyecto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f9a710795a29481740bf85390cc7122cc801a22
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104274707"
---
# <a name="loading-a-project-file"></a>Cargar un archivo de proyecto

\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]

Para cargar un archivo de proyecto, necesita dos componentes: el analizador XML y una escala de tiempo vacía. El analizador XML Lee un archivo de proyecto XML y crea cada objeto definido en el archivo. A continuación, inserta los objetos en la escala de tiempo y establece los atributos de la escala de tiempo, como la velocidad de fotogramas predeterminada. En el ejemplo de código siguiente se carga un archivo.


```C++
HRESULT         hr;
IAMTimeline     *pTL = NULL;
IXml2Dex        *pXML = NULL; 
hr = CoCreateInstance(CLSID_AMTimeline, NULL, CLSCTX_INPROC_SERVER, 
            IID_IAMTimeline, (void**)&pTL);
hr = CoCreateInstance(CLSID_Xml2Dex, NULL, CLSCTX_INPROC_SERVER, 
            IID_IXml2Dex, (void**)&pXML);
BSTR bstrFile = SysAllocStringLen(OLESTR("C:\\example.xtl"), 15);
hr = pXML->ReadXMLFile(pTL, bstrFile); 
SysFreeString(bstrFile);
pXML->Release();
```



El analizador expone la interfaz [**IXml2Dex**](ixml2dex.md) , que contiene métodos para cargar y guardar archivos de proyecto. La escala de tiempo expone la interfaz [**IAMTimeline**](iamtimeline.md) , que contiene métodos para manipular la escala de tiempo y crear nuevos objetos Timeline. Llame a la función **CoCreateInstance** para crear cada componente, como se muestra. Recuerde que, al crear una nueva instancia, está incrementando el recuento de referencias en la interfaz. Para evitar pérdidas de memoria, libere siempre una interfaz cuando esté a través de ella. En este ejemplo, el puntero a **IXml2Dex** no es necesario para nada más, por lo que puede liberar la interfaz. El puntero a **IAMTimeline** sigue siendo necesario para obtener una vista previa de la escala de tiempo.

El método [**IXml2Dex:: ReadXMLFile**](ixml2dex-readxmlfile.md) lee el archivo especificado y rellena la escala de tiempo con los objetos definidos en el archivo. El nombre de archivo se especifica mediante un valor **BSTR** . Para acortar el ejemplo, el nombre de archivo en el ejemplo se proporciona como una cadena literal. Normalmente, se obtiene de un cuadro de diálogo Abrir archivo o algo similar.

Si el método **ReadXml** se realiza correctamente, devuelve un código de éxito. De lo contrario, devuelve un código de error como VFW \_ E \_ no es un formato de \_ archivo válido \_ . Compruebe siempre el valor devuelto para controlar correctamente las condiciones de error. De nuevo, para mayor brevedad, el código de ejemplo no comprueba si hay errores.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Cargar y obtener una vista previa de un proyecto](loading-and-previewing-a-project.md)
</dt> </dl>

 

 



