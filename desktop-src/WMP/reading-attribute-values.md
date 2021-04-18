---
title: Leer valores de atributo
description: Leer valores de atributo
ms.assetid: 5f791f47-472e-409f-b716-2ace11f34742
keywords:
- Windows Media Player, atributos para elementos multimedia
- Modelo de objetos de Windows Media Player, atributos para elementos multimedia
- modelo de objetos, atributos para elementos multimedia
- Windows Media Player Mobile, atributos para elementos multimedia
- Control ActiveX de Windows Media Player, atributos para elementos multimedia
- Control ActiveX móvil de Windows Media Player, atributos para elementos multimedia
- Control ActiveX, atributos para elementos multimedia
- Biblioteca de Media Player de Windows, atributos para elementos multimedia
- Biblioteca, atributos para elementos multimedia
- atributos, leer valores
- leer valores de atributo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d527429b71cff5594c127b3ad2bfb82b3f3b2ef
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704755"
---
# <a name="reading-attribute-values"></a>Leer valores de atributo

Los atributos que puede encontrar en la biblioteca y en los archivos de Windows Media tienen nombres predefinidos. Puede escribir código que recupere el valor de un atributo pasando el nombre de ese atributo a un *medio*. **getItemInfo** o *multimedia*. **getItemInfoByType**. También puede escribir código que recupere los valores de todos los atributos de un archivo o un elemento.

En el siguiente ejemplo de C# se recupera el valor del atributo **title** y se muestra en un cuadro de mensaje. En este ejemplo, el objeto **Player** se definió como AxWMPLib. AxWindowsMediaPlayer Player.


```C++
IWMPMedia media;
string strAttribValue = "";

// Initialize the media object
media = Player.currentMedia;

// Retrieve the object's Title attribute
strAttribValue = media.getItemInfo("Title");

// Display the title
if (strAttribValue != "")
{
    MessageBox.Show("Current title: " + strAttribValue);
}

```



En la llamada a **getItemInfoByType**, el segundo parámetro es una cadena que especifica el idioma. Si pasa una cadena vacía como se muestra en este ejemplo, el método recupera el valor en el idioma predeterminado. Para obtener información sobre el tercer parámetro, vea [atributos con varios valores](attributes-with-multiple-values.md).

En el siguiente ejemplo de C# se recuperan los valores de un atributo determinado en el elemento multimedia actual. Devuelve estos valores como una cadena delimitada por signos de punto y coma. Tenga en cuenta que para los atributos representados como objetos, como **WM/Letras \_ sincronizadas**, **WM/imagen** y **WM/UserWebURL**, la función devuelve una cadena vacía.


```C++
private string getAttributeValues(string strAttrName, IWMPMedia3 media)
{
    string strAttrValue = "";
    int iAttrCount = 0;

    if (media != null)
    {
        // Retrieve the count of values for this attribute
        iAttrCount = media.getAttributeCountByType(strAttrName, "");

        // Retrieve the values
        for (int i = 0; i < iAttrCount; i++)
        {
            strAttrValue += media.getItemInfoByType(strAttrName, "", i);
            strAttrValue += ";";
        }
    }

    // Return the resulting string
    return strAttrValue;
}

```



El tercer argumento que se pasa al método **getItemInfoByType** es el índice de un atributo determinado en un conjunto de atributos con el mismo nombre.

Puede usar código similar para recuperar los atributos que tienen nombres únicos. En estos casos, **getAttributeCountByType** devuelve 1. En el ejemplo mostrado anteriormente, la llamada a **getItemInfoByType** se ejecutaría una sola vez.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Cambiar valores de atributo**](changing-attribute-values.md)
</dt> <dt>

[**Atributos de elemento multimedia**](media-item-attributes.md)
</dt> <dt>

[**Objeto multimedia**](media-object.md)
</dt> <dt>

[**Leer valores de atributo de un CD o DVD**](reading-attribute-values-from-a-cd-or-dvd.md)
</dt> </dl>

 

 




