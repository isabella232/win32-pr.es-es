---
title: Lectura de valores de atributo
description: Lectura de valores de atributo
ms.assetid: 5f791f47-472e-409f-b716-2ace11f34742
keywords:
- Reproductor de Windows Media,attributes para elementos multimedia
- Reproductor de Windows Media modelo de objetos,atributos para elementos multimedia
- object model,attributes for media items
- Reproductor de Windows Media Móvil, atributos para elementos multimedia
- Reproductor de Windows Media ActiveX control,atributos para elementos multimedia
- Reproductor de Windows Media Control de ActiveX móvil,atributos para elementos multimedia
- ActiveX control,atributos para elementos multimedia
- Reproductor de Windows Media biblioteca,atributos para elementos multimedia
- library,attributes para elementos multimedia
- attributes,reading values
- lectura de valores de atributo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d527429b71cff5594c127b3ad2bfb82b3f3b2ef
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070936"
---
# <a name="reading-attribute-values"></a>Lectura de valores de atributo

Los atributos que puede encontrar en la biblioteca y en Windows archivos multimedia tienen nombres predefinidos. Puede escribir código que recupere el valor de un atributo pasando el nombre de ese atributo a *Media*. **getItemInfo o** *Media*. **getItemInfoByType**. También puede escribir código que recupere los valores de todos los atributos de un archivo o elemento.

En el siguiente ejemplo de C# se recupera el valor del atributo **Title** y se muestra en un cuadro de mensaje. En este ejemplo, el **objeto Player** se definió como axWMPLib.AxWindowsMediaPlayer Player.


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



En la llamada a **getItemInfoByType**, el segundo parámetro es una cadena que especifica el idioma. Si pasa una cadena vacía como se muestra en este ejemplo, el método recupera el valor en el idioma predeterminado. Para obtener información sobre el tercer parámetro, vea [Atributos con varios valores.](attributes-with-multiple-values.md)

En el siguiente ejemplo de C# se recuperan los valores de un atributo determinado en el elemento multimedia actual. Devuelve estos valores como una cadena delimitada por punto y coma. Tenga en cuenta que para los atributos representados como objetos, como **WM/Se sincronizan las \_** sincronizaciones, **WM/Picture** y **WM/UserWebURL,** la función devuelve una cadena vacía.


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



El tercer argumento pasado al **método getItemInfoByType** es el índice de un atributo determinado en un conjunto de atributos con el mismo nombre.

Puede usar código similar para recuperar atributos que tienen nombres únicos. En esos casos, **getAttributeCountByType** devuelve 1. En el ejemplo mostrado anteriormente, la llamada a **getItemInfoByType** solo se ejecutaría una vez.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Cambiar valores de atributo**](changing-attribute-values.md)
</dt> <dt>

[**Atributos de elementos multimedia**](media-item-attributes.md)
</dt> <dt>

[**Objeto multimedia**](media-object.md)
</dt> <dt>

[**Lectura de valores de atributo de un CD o DVD**](reading-attribute-values-from-a-cd-or-dvd.md)
</dt> </dl>

 

 




