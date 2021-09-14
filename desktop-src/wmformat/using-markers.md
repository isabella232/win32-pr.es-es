---
title: Uso de marcadores
description: Uso de marcadores
ms.assetid: b801c985-4ec7-441e-9f8a-40c69b1299a9
keywords:
- Windows SDK de formato multimedia, marcadores
- Formato de sistemas avanzados (ASF), marcadores
- ASF (formato de sistemas avanzados),marcadores
- Formato de sistemas avanzados (ASF), buscar marcadores
- ASF (formato de sistemas avanzados), buscar marcadores
- marcadores, acerca de
- marcadores, agregar
- marcadores, quitar
- marcadores, recuperar
- marcadores, buscar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44cc585b8c71e3bfbae85953650809ad031d36a2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127247221"
---
# <a name="using-markers"></a>Uso de marcadores

Un *marcador* es un punto con nombre dentro de un archivo ASF. Cada marcador consta de un nombre y una hora asociada, medidos como un desplazamiento desde el inicio del archivo. Una aplicación puede usar marcadores para asignar nombres a varios puntos del contenido, mostrar esos nombres al usuario y, a continuación, buscar en las posiciones del marcador. Una aplicación puede agregar o quitar marcadores de un archivo ASF existente.

La [**interfaz IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) contiene métodos para trabajar con marcadores. El objeto del editor de metadatos admite la adición y eliminación de marcadores. Los objetos de escritor y lector pueden recuperar marcadores, pero no pueden agregar ni quitar marcadores.

## <a name="adding-markers"></a>Agregar marcadores

Para agregar un marcador, consulte el editor de metadatos para la **interfaz IWMHeaderInfo.** A continuación, llame al método [**IWMHeaderInfo::AddMarker,**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-addmarker) especificando el nombre del marcador como una cadena de caracteres anchos y la hora en unidades de 100 nanosegundos. El tiempo no debe superar la duración del archivo. Dos marcadores pueden tener la misma hora.

En el ejemplo siguiente se agregan varios marcadores a un archivo:


```C++
IWMMetadataEditor *pEdit = 0;
IWMHeaderInfo     *pInfo = 0;

// Create the metadata editor object.

WMCreateEditor(&pEdit);
pEdit->Open(L"C:\\example.wmv");
pEdit->QueryInterface(IID_IWMHeaderInfo, (void**)&pInfo);

// Add the markers. Note that we add the last ones first. Do this when possible
// for improved performance when writing the markers to the file.
hr = pInfo->AddMarker(L"End",  520000000);   // 52 sec.
hr = pInfo->AddMarker(L"Segue",  350000000); // 35 sec.
hr = pInfo->AddMarker(L"Intro",  15000000);  // 1.5 sec.

// Commit changes and clean up.

pEdit->Flush();
pEdit->Close(); 
pInfo->Release();
pEdit->Release();

```



## <a name="removing-markers"></a>Quitar marcadores

Para quitar un marcador, llame a [**IWMHeaderInfo::RemoveMarker**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-removemarker)y especifique el índice del marcador que se quitará. Los marcadores se ordenan automáticamente en orden de tiempo creciente, por lo que el índice 0 siempre es el primer marcador. Tenga en cuenta que **al llamar a RemoveMarker** se cambian los números de índice de los marcadores siguientes. El código siguiente, donde *pInfo* es un puntero a una **interfaz IWMHeaderInfo,** quita todos los marcadores de un archivo:


```C++
WORD count = 0;
pInfo->GetMarkerCount(&count);
while (count--)
{
    pInfo->RemoveMarker(0);
}

```



## <a name="retrieving-markers"></a>Recuperar marcadores

Para recuperar el nombre y la hora de un marcador, realice los pasos siguientes:

1.  Llame al [**método IWMHeaderInfo::GetMarkerCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getmarkercount) para determinar cuántos marcadores contiene el archivo.
2.  Recupere el tamaño de la cadena necesaria para contener el nombre del marcador. Para ello, llame al [**método IWMHeaderInfo::GetMarker.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getmarker) Especifique el índice del marcador que se recuperará y **NULL para** el búfer de cadena (el *parámetro pwszMarkerName).* El método devuelve la longitud de la cadena, incluido el carácter \\ "0" final, en el *parámetro pcchMarkerNameLen.*
3.  Asigne una cadena de caracteres anchos para recibir el nombre.
4.  Vuelva **a llamar a GetMarker,** pero esta vez pase la dirección de la cadena en el parámetro *pwszMarkerName.* El método escribe el nombre del marcador en la cadena y devuelve la hora del marcador en el *parámetro pcnsMarkerTime.*

El código siguiente recorre cada marcador en orden y recupera el nombre y la hora:


```C++
WORD cMarkers = 0;
HRESULT hr = pInfo->GetMarkerCount(&cMarkers);

WCHAR *wszName = 0;
WORD  len = 0;
for (WORD iMarker = 0; iMarker < cMarkers; ++iMarker)
{
    QWORD rtTime = 0;
    WORD req_len = 0;
    hr = pInfo->GetMarker(iMarker, 0, &req_len, &rtTime);
    
    // Reallocate if necessary.
    if (len < req_len)
    {
        delete[] wszName;
        wszName = new WCHAR[req_len];
        len = req_len;
    }
    hr = pInfo->GetMarker(iMarker, wszName, &req_len, &rtTime);
    // Display the name...
}
delete[] wszName;

```



## <a name="seeking-to-a-marker"></a>Búsqueda de un marcador

Para iniciar la reproducción desde una ubicación de marcador, llame al método [**IWMReaderAdvanced2::StartAtMarker**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-startatmarker) del objeto lector, especificando el índice del marcador. Los parámetros restantes son idénticos a los del [**método IWMReader::Start.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-start) En el ejemplo siguiente se consulta al lector la [**interfaz IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) y se busca en el primer marcador.


```C++
IWMReaderAdvanced2 *pReader2 = 0
WORD iMarkerIndex = 0;
hr = pReader->QueryInterface(IID_IWMReaderAdvanced2, (void**)&pReader2);
if (SUCCEEDED(hr))
{
    hr = pPlayer2->StartAtMarker(iMarkerIndex, 0, 1.0, 0);
    pPlayer2->Release();
}

```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IWMHeaderInfo (interfaz)**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)
</dt> <dt>

[**IWMReaderAdvanced2::StartAtMarker**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-startatmarker)
</dt> <dt>

[**Trabajar con metadatos**](working-with-metadata.md)
</dt> </dl>

 

 




