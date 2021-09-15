---
description: Insertar una fuente es la técnica para agrupar un documento y las fuentes que contiene en un archivo para su transmisión a otro equipo.
ms.assetid: ded409f1-5bd9-411b-b905-fc49c484786a
title: Fuentes incrustadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83fb8ab821afa5f44ded05a4a61a53439b8db9fc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127475948"
---
# <a name="embedded-fonts"></a>Fuentes incrustadas

Insertar una fuente es la técnica para agrupar un documento y las fuentes que contiene en un archivo para su transmisión a otro equipo. La inserción de una fuente garantiza que una fuente especificada en un archivo transmitido estará presente en el equipo que recibe el archivo. Sin embargo, no todas las fuentes se pueden mover de un equipo a otro, ya que la mayoría de las fuentes solo tienen licencia para un equipo a la vez. Solo se pueden incrustar fuentes TrueType y OpenType.

Las aplicaciones deben insertar una fuente en un documento solo cuando lo solicite un usuario. Una aplicación no se puede distribuir junto con documentos que contienen fuentes incrustadas, ni puede contener una fuente incrustada. Cada vez que una aplicación distribuye una fuente, en cualquier formato, se deben confirmar los derechos propietarios del propietario de la fuente.

Puede ser una infracción de los derechos de propiedad de un proveedor de fuentes o del contrato de licencia de usuario insertar cualquier fuente en la que no se permita la inserción o no observar las siguientes directrices sobre la inserción de fuentes. La licencia de una fuente solo puede conceder permiso de lectura y escritura para que una fuente se instale y se utilice en el equipo de destino. O bien, la licencia puede conceder permiso de solo lectura. El permiso de solo lectura permite que el equipo de destino vea e imprima un documento (pero no lo modifique); Los documentos con fuentes incrustadas de solo lectura son en sí mismos de solo lectura. Es posible que las fuentes incrustadas de solo lectura no se desasoyen del documento y se instalen en el equipo de destino.

Una aplicación puede determinar el estado de la licencia llamando a la función [**GetOutlineTextMetrics**](/windows/desktop/api/Wingdi/nf-wingdi-getoutlinetextmetricsa) y examinando el **miembro otmfsType** de la [**estructura OUTLINETEXTMETRIC.**](/windows/desktop/api/Wingdi/ns-wingdi-outlinetextmetrica) Si se establece el bit 1 **de otmfsType,** no se permite la inserción para la fuente. Si el bit 1 está claro, se puede incrustar la fuente. Si se establece el bit 2, la inserción es de solo lectura.

Para insertar una fuente TrueType, una aplicación puede usar la [**función GetFontData**](/windows/desktop/api/Wingdi/nf-wingdi-getfontdata) para leer el archivo de fuente. Establecer los *parámetros dwTable* y *dwOffset* de [**GetFontData**](/windows/win32/api/wingdi/nf-wingdi-getfontdata) en 0L y el parámetro *cbData* en 1L garantiza que la aplicación lee todo el archivo de fuente desde el principio.

Hay varias funciones disponibles para insertar fuentes OpenType en función del ancho de los caracteres y de dónde residen los datos de fuente. Para insertar una fuente Unicode OpenType que reside en un contexto de dispositivo, una aplicación puede usar [**TTEmbedFont**](/windows/desktop/api/T2embapi/nf-t2embapi-ttembedfont). Para insertar una fuente UCS-4 de OpenType que reside en un contexto de dispositivo, una aplicación puede usar [**TTEmbedFontEx**](/windows/desktop/api/T2embapi/nf-t2embapi-ttembedfontex). Para insertar una fuente Unicode OpenType que reside en un archivo de fuente, una aplicación puede usar [**TTEmbedFontFromFile**](/windows/desktop/api/T2embapi/nf-t2embapi-ttembedfontfromfilea). Para obtener información adicional sobre la inserción de fuentes OpenType, consulte [la referencia de incrustación de fuentes](font-embedding-reference.md).

Una vez que una aplicación recupera los datos de fuente, puede almacenar los datos con el documento mediante cualquier formato aplicable. La mayoría de las aplicaciones compilan un directorio de fuentes en el documento, donde se enumeran las fuentes incrustadas y si la inserción es de solo lectura o escritura o de solo lectura. Una aplicación puede usar los **miembros otmpStyleName** y **otmFamilyName** de la [**estructura OUTLINETEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-outlinetextmetrica) para identificar la fuente.

Si el bit de solo lectura se establece para la fuente incrustada, las aplicaciones deben cifrar los datos de fuente antes de almacenarlos con el documento. El método de cifrado no tiene que ser complicado; Por ejemplo, el uso del operador XOR para combinar los datos de fuente con una constante definida por la aplicación es adecuado y rápido.

 

 
