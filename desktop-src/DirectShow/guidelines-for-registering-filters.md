---
description: Directrices para registrar filtros
ms.assetid: 05945937-9e01-4930-ae95-1931a711b55e
title: Directrices para registrar filtros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 221cadf6fb4806a2fa5c5b2cc4fd9abf423cec426ec23cd76b0bc642080852af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119905365"
---
# <a name="guidelines-for-registering-filters"></a>Directrices para registrar filtros

La información del Registro de filtros determina cómo funciona filter Graph Manager durante [intelligent Conectar](intelligent-connect.md). Por lo tanto, afecta a todas las aplicaciones escritas DirectShow, no solo a las que usarán el filtro. Debe asegurarse de que el filtro se comporta correctamente siguiendo estas directrices.

1.  ¿Necesita los datos de filtro en el Registro? Para muchos filtros personalizados, no hay ninguna razón para que el filtro sea visible para el Asignador de filtros o el Enumerador de dispositivos del sistema. Siempre que registre el archivo DLL, la aplicación puede crear el filtro mediante **CoCreateInstance**. En ese caso, simplemente omita la estructura [**FILTER \_ de AMOVIESETUP**](amoviesetup-filter.md) de la plantilla de generador. (Un inconveniente es que el filtro no estará visible en GraphEdit. Para evitarlo, puede crear una categoría privada "Testing" mediante el [**método IFilterMapper2::CreateCategory.**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-createcategory) Solo debe hacer esto para las compilaciones de depuración).
2.  Elija la categoría de filtro correcta. La categoría predeterminada "DirectShow filtros" es para filtros de uso general. Siempre que sea necesario, registre el filtro en una categoría más específica. Cuando [**IFilterMapper2 busca**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) un filtro, omite cualquier categoría cuyo valor sea NO USAR NI USAR NI \_ MUCHO \_ \_ MENOS. Las categorías no diseñadas para la reproducción normal tienen pocos valores.
3.  Evite especificar MEDIATYPE None, MEDIASUBTYPE None o GUID NULL en la información de MEDIATYPE de \_ \_ \_ [**AMOVIESETUP \_**](amoviesetup-mediatype.md) para un pin. **IFilterMapper2 los** trata como caracteres comodín, lo que puede ralentizar el proceso de creación de grafos.
4.  Elija el valor más bajo posible. Estas son algunas directrices:

    | Tipo de filtro                                                                                       | Recomendación                                                                                   |
    |------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
    | Representador predeterminado                                                                                     | PREFERRED \_ PREFERRED. Sin embargo, para los tipos de medios estándar, un representador personalizado nunca debe ser el valor predeterminado. |
    | Representador no predeterminado                                                                                 | NO USE EL VALOR DE NO \_ \_ UTILIZAR O UNLIKELY \_ \_ UNLIKELY                                                              |
    | Mux                                                                                                  | NO USE EL VALOR DE NO \_ \_ \_ USE.                                                                                 |
    | Descodificador                                                                                              | NORMAL DE LA OPERACIÓN DE \_ NORMALIZACIÓN                                                                                       |
    | Desenlazador, analizador                                                                                      | PROCEDIMIENTO \_ NORMAL o inferior                                                                              |
    | Filtro de propósito especial; cualquier filtro creado directamente por la aplicación                       | NO USE EL VALOR DE NO \_ \_ \_ USE.                                                                                 |
    | Capturar                                                                                              | NO USE EL VALOR DE NO \_ \_ \_ USE.                                                                                 |
    | Filtro "Reserva"; por ejemplo, el [filtro convertidor de espacios de colores](color-space-converter-filter.md) | NO ES \_ PROBABLE QUE SE PRODUZCA UN GRAN                                                                                     |

    

     

    Si va a dar a un filtro un crédito de NO USAR NO USE, considere si necesita \_ registrar esta información en primer \_ \_ lugar. (Vea el elemento 1).

5.  No registre un filtro en la categoría "DirectShow" que acepte RGB de 24 bits. El filtro interferirá con el filtro Convertidor de espacios de colores.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Cómo registrar filtros de DirectShow datos](how-to-register-directshow-filters.md)
</dt> </dl>

 

 



