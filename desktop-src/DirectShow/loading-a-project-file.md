---
description: Carga de un Project archivo
ms.assetid: f8d142bd-e51d-4714-893b-8e3d02506891
title: Carga de un Project archivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f9a710795a29481740bf85390cc7122cc801a22
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063196"
---
# <a name="loading-a-project-file"></a>Carga de un Project archivo

\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]

Para cargar un archivo de proyecto, necesita dos componentes: el analizador XML y una escala de tiempo vacía. El analizador XML lee un archivo de proyecto XML y crea cada objeto definido en el archivo. A continuación, inserta los objetos en la escala de tiempo y establece los atributos de escala de tiempo, como la velocidad de fotogramas predeterminada. En el ejemplo de código siguiente se carga un archivo .


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



El analizador expone la interfaz [**IXml2Dex,**](ixml2dex.md) que contiene métodos para cargar y guardar archivos de proyecto. La escala de tiempo expone la [**interfaz IAMTimeline,**](iamtimeline.md) que contiene métodos para manipular la escala de tiempo y crear nuevos objetos de escala de tiempo. Llame a **la función CoCreateInstance** para crear cada componente, como se muestra. Recuerde que al crear una nueva instancia, está incrementando el recuento de referencias en la interfaz . Para evitar pérdidas de memoria, libere siempre una interfaz cuando haya pasado por ella. En este ejemplo, el puntero a **IXml2Dex** no es necesario para nada más, por lo que puede liberar la interfaz . El puntero a **IAMTimeline** sigue siendo necesario para obtener una vista previa de la escala de tiempo.

El [**método IXml2Dex::ReadXMLFile**](ixml2dex-readxmlfile.md) lee el archivo especificado y rellena la escala de tiempo con los objetos definidos en el archivo. El nombre de archivo se especifica mediante un **valor BSTR.** Para acortar el ejemplo, el nombre de archivo del ejemplo se da como una cadena literal. Normalmente, se obtiene de un cuadro de diálogo Abrir archivo o algo similar.

Si el **método ReadXML** se realiza correctamente, devuelve un código correcto. De lo contrario, devuelve un código de error como VFW \_ E \_ INVALID FILE \_ \_ FORMAT. Compruebe siempre el valor devuelto para controlar las condiciones de error correctamente. De nuevo por brevedad, el código de ejemplo no comprueba si hay errores.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Carga y vista previa de un Project](loading-and-previewing-a-project.md)
</dt> </dl>

 

 



