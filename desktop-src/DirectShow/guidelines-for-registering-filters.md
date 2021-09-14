---
description: Directrices para registrar filtros
ms.assetid: 05945937-9e01-4930-ae95-1931a711b55e
title: Directrices para registrar filtros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ed616d90c17d232995994d8ceccfdc72d022d56
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127169965"
---
# <a name="guidelines-for-registering-filters"></a>Directrices para registrar filtros

La información del Registro de filtros determina cómo funciona filter Graph Manager durante [intelligent Conectar](intelligent-connect.md). Por lo tanto, afecta a todas las aplicaciones escritas DirectShow, no solo a las que usarán el filtro. Debe asegurarse de que el filtro se comporta correctamente siguiendo estas instrucciones.

1.  ¿Necesita los datos de filtro en el Registro? Para muchos filtros personalizados, no hay ninguna razón para que el filtro sea visible para el Asignador de filtros o el Enumerador de dispositivos del sistema. Siempre que registre el archivo DLL, la aplicación puede crear el filtro mediante **CoCreateInstance**. En ese caso, simplemente omita la [**estructura FILTER de AMOVIESETUP \_**](amoviesetup-filter.md) de la plantilla de generador. (Un inconveniente es que el filtro no estará visible en GraphEdit. Para evitarlo, puede crear una categoría privada "Testing" mediante el [**método IFilterMapper2::CreateCategory.**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-createcategory) Solo debe hacer esto para las compilaciones de depuración).
2.  Elija la categoría de filtro correcta. La categoría predeterminada "DirectShow filtros" es para los filtros de uso general. Siempre que sea necesario, registre el filtro en una categoría más específica. Cuando [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) busca un filtro, pasa por alto cualquier categoría cuyo valor sea NO USAR NI \_ MUCHO \_ \_ MENOS. Las categorías no diseñadas para la reproducción normal tienen poco peso.
3.  Evite especificar MEDIATYPE None, MEDIASUBTYPE None o GUID NULL en la información de MEDIATYPE de \_ \_ \_ [**AMOVIESETUP \_**](amoviesetup-mediatype.md) para un pin. **IFilterMapper2 los** trata como caracteres comodín, lo que puede ralentizar el proceso de creación de grafos.
4.  Elija el valor más bajo posible. Estas son algunas directrices:

    | Tipo de filtro                                                                                       | Recomendación                                                                                   |
    |------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
    | Representador predeterminado                                                                                     | PREFERRED \_ PREFERRED. Sin embargo, para los tipos de medios estándar, un representador personalizado nunca debe ser el valor predeterminado. |
    | Representador no predeterminado                                                                                 | NO USE EL VALOR DE NO \_ \_ USE O UNLIKELY \_ \_ UNLIKELY.                                                              |
    | Mux                                                                                                  | NO USE LA OPCIÓN DE \_ \_ NO \_ USAR.                                                                                 |
    | Descodificador                                                                                              | PROCEDIMIENTO \_ NORMAL                                                                                       |
    | Desenlazador, analizador                                                                                      | PROCEDIMIENTO \_ NORMAL o inferior                                                                              |
    | Filtro de propósito especial; cualquier filtro creado directamente por la aplicación                       | NO USE LA OPCIÓN DE \_ \_ NO \_ USAR.                                                                                 |
    | Capturar                                                                                              | NO USE LA OPCIÓN DE \_ \_ NO \_ USAR.                                                                                 |
    | Filtro "Reserva"; por ejemplo, el [filtro convertidor de espacios de colores](color-space-converter-filter.md) | NO ES \_ PROBABLE QUE SE PRODUZCAN                                                                                     |

    

     

    Si va a dar a un filtro una virtud de NO USAR NO USE, considere si necesita \_ registrar esta información en primer \_ \_ lugar. (Vea el elemento 1).

5.  No registre un filtro en la categoría "DirectShow filtros" que acepte RGB de 24 bits. El filtro interferirá con el filtro Convertidor de espacios de color.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registro de filtros DirectShow filtros](how-to-register-directshow-filters.md)
</dt> </dl>

 

 



