---
description: Directrices para registrar filtros
ms.assetid: 05945937-9e01-4930-ae95-1931a711b55e
title: Directrices para registrar filtros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ed616d90c17d232995994d8ceccfdc72d022d56
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104151962"
---
# <a name="guidelines-for-registering-filters"></a>Directrices para registrar filtros

La información del registro de filtros determina cómo funciona el administrador de gráficos de filtro durante la [conexión inteligente](intelligent-connect.md). Por lo tanto, afecta a todas las aplicaciones escritas para DirectShow, no solo a las que usarán el filtro. Debe asegurarse de que el filtro se comporta correctamente siguiendo estas instrucciones.

1.  ¿Necesita los datos de filtro en el registro? En el caso de muchos filtros personalizados, no hay ninguna razón para que el filtro sea visible para el asignador de filtros o el enumerador de dispositivos del sistema. Siempre que registre el archivo DLL, la aplicación puede crear el filtro mediante **CoCreateInstance**. En ese caso, simplemente omita la estructura del [**\_ filtro AMOVIESETUP**](amoviesetup-filter.md) de la plantilla de fábrica. (Una desventaja es que el filtro no será visible en GraphEdit. Para solucionar este tema, puede crear una categoría de "pruebas" privada mediante el método [**IFilterMapper2:: CreateCategory**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-createcategory) . Solo debe hacer esto para las compilaciones de depuración).
2.  Elija la categoría de filtro correcta. La categoría predeterminada "filtros de DirectShow" es para los filtros de uso general. Siempre que sea necesario, registre el filtro en una categoría más específica. Cuando [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) busca un filtro, omite cualquier categoría cuyo mérito sea mérito \_ \_ no \_ use o Less. Las categorías que no están destinadas a la reproducción normal tienen un mérito bajo.
3.  Evite especificar MEDIATYPE \_ None, MEDIASUBTYPE \_ None o GUID \_ null en la información de un valor de [**\_ mediatype de AMOVIESETUP**](amoviesetup-mediatype.md) para un PIN. **IFilterMapper2** los trata como caracteres comodín, lo que puede ralentizar el proceso de creación de gráficos.
4.  Elija el valor de mérito más bajo posible. Estas son algunas directrices:

    | Tipo de filtro                                                                                       | Mérito recomendado                                                                                   |
    |------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
    | Representador predeterminado                                                                                     | MÉRITO \_ recomendado. En el caso de los tipos de medios estándar, sin embargo, un representador personalizado nunca debe ser el valor predeterminado. |
    | Representador no predeterminado                                                                                 | MÉRITO \_ \_ no se \_ utiliza o no es \_ probable que el mérito                                                              |
    | MUX                                                                                                  | MÉRITO \_ \_ no se \_ usa                                                                                 |
    | Descodificador                                                                                              | MÉRITO \_ normal                                                                                       |
    | Spitter, analizador                                                                                      | MÉRITO \_ normal o inferior                                                                              |
    | Filtro de propósito especial; cualquier filtro creado directamente por la aplicación                       | MÉRITO \_ \_ no se \_ usa                                                                                 |
    | Capturar                                                                                              | MÉRITO \_ \_ no se \_ usa                                                                                 |
    | Filtro de "reserva"; por ejemplo, el [filtro del convertidor de espacio de colores](color-space-converter-filter.md) | MÉRITO \_ improbable                                                                                     |

    

     

    Si está asignando un filtro, no se debe \_ \_ \_ usar el mérito, tenga en cuenta si tiene que registrar esta información en primer lugar. (Vea el elemento 1).

5.  No registre un filtro en la categoría "filtros de DirectShow" que acepte RGB de 24 bits. El filtro interferirá con el filtro del convertidor de espacio de colores.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Cómo registrar filtros de DirectShow](how-to-register-directshow-filters.md)
</dt> </dl>

 

 



