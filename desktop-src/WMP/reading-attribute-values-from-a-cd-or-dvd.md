---
title: Leer valores de atributo de un CD o DVD
description: Leer valores de atributo de un CD o DVD
ms.assetid: 441916fb-f66d-4a12-a95c-b47561c93e64
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
ms.openlocfilehash: 8909a752e9a974e4959be8ecd933d4bb3f1bfd4a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357510"
---
# <a name="reading-attribute-values-from-a-cd-or-dvd"></a><span data-ttu-id="01ffc-114">Leer valores de atributo de un CD o DVD</span><span class="sxs-lookup"><span data-stu-id="01ffc-114">Reading Attribute Values from a CD or DVD</span></span>

<span data-ttu-id="01ffc-115">A lo largo de este tema, el objeto **Player** se definió de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="01ffc-115">Throughout this topic, the **Player** object was defined in the following manner:</span></span>


```C++
AxWMPLib.AxWindowsMediaPlayer Player;
using WMPLib;

```



<span data-ttu-id="01ffc-116">En el siguiente código de ejemplo de C# se recuperan los valores de todos los atributos del disco actual que se encuentra en la unidad y se escriben en un archivo.</span><span class="sxs-lookup"><span data-stu-id="01ffc-116">The following C# example code retrieves the values of all attributes in the current disc that is in the drive and writes them to a file.</span></span>


```C++
private void logDiscAttributes()
{
    int iCDCount = 0; // Count of CD and DVD drives
    int iAttrCount = 0; // Attribute count.
    int iPLCount = 0; // Playlist item count.

    IWMPCdromCollection cdCollection;
    IWMPPlaylist playlist;
    IWMPMedia media;
    string strAttribName = "";
    string strAttribValue = "";
    string strText = "";

    // Create a StreamWriter object to write
    // the output to a file.
    StreamWriter sw = new StreamWriter(strOutFile, true);

    cdCollection = Player.cdromCollection;
    iCDCount = cdCollection.count;

    // Loop through the CD and DVD drives.
    for (int i = 0; i < iCDCount; i++)
    {
        playlist = cdCollection.Item(i).Playlist;

        // Loop through the playlist attributes.
        iAttrCount = playlist.attributeCount;
        for (int j = 0; j < iAttrCount; j++)
        {
            strText += "Playlist Attribute: \t";
            strAttribName = playlist.get_attributeName(j);
            strText += "\t" + strAttribName + "\t";
            strAttribValue = playlist.getItemInfo(strAttribName);
            strText += strAttribValue + "\n";
        }

        // Loop through the playlist.
        iPLCount = playlist.count;
        for (int k = 0; k < iPLCount; k++)
        {
            media = playlist.get_Item(k);

            // Loop through the media attributes.
            iAttrCount = media.attributeCount;
            for (int m = 0; m < iAttrCount; m++)
            {
                strText += "Track or Chapter [" + m.ToString() + "]";
                strAttribName = media.getAttributeName(m);
                strText += "\t" + strAttribName + "\t";
                strText += "Read Only: " + media.isReadOnlyItem(strAttribName) + "\t";
                strAttribValue = media.getItemInfo(strAttribName);
                strText += strAttribValue + "\n";
            }
        }
    }

    sw.Write(strText);
    sw.Close();

    MessageBox.Show(strOutFile + " created");
}

```



## <a name="related-topics"></a><span data-ttu-id="01ffc-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="01ffc-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="01ffc-118">**Atributos de elemento multimedia**</span><span class="sxs-lookup"><span data-stu-id="01ffc-118">**Media Item Attributes**</span></span>](media-item-attributes.md)
</dt> <dt>

[<span data-ttu-id="01ffc-119">**Objeto multimedia**</span><span class="sxs-lookup"><span data-stu-id="01ffc-119">**Media Object**</span></span>](media-object.md)
</dt> </dl>

 

 




