---
description: Introducción al desarrollo de filtros de DirectShow
ms.assetid: d5162ea4-ef37-4993-a82c-782f03b08c64
title: Introducción al desarrollo de filtros de DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a42c5d2437b32f521b0efc39775f186267d3c99
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105686332"
---
# <a name="introduction-to-directshow-filter-development"></a>Introducción al desarrollo de filtros de DirectShow

En esta sección se proporciona una breve descripción de las tareas relacionadas con el desarrollo de un filtro DirectShow personalizado. También se proporcionan vínculos a temas que describen estas tareas con mayor detalle. Antes de leer esta sección, lea los temas [sobre DirectShow](about-directshow.md), que describen la arquitectura de DirectShow general.

**Biblioteca de clases base de DirectShow**

El SDK de DirectShow incluye un conjunto de clases de C++ para escribir filtros. Aunque no son necesarios, estas clases son la manera recomendada de escribir un nuevo filtro. Para usar las clases base, compílelo en una biblioteca estática y vincule el archivo. lib al proyecto, tal como se describe en [crear filtros de DirectShow](building-directshow-filters.md).

La biblioteca de clases base define una clase raíz para los filtros, la clase [**CBaseFilter**](cbasefilter.md) . Otras clases se derivan de **CBaseFilter** y se especializan en determinados tipos de filtros. Por ejemplo, la clase [**CTransformFilter**](ctransformfilter.md) está diseñada para los filtros de transformación. Para crear un nuevo filtro, implemente una clase que herede de una de las clases de filtro. Por ejemplo, la declaración de clase podría ser la siguiente:


```C++
class CMyFilter : public CTransformFilter
{
private:
    /* Declare variables and methods that are specific to your filter.
public:
    /* Override various methods in CTransformFilter */
};
```



Para obtener más información acerca de las clases base de DirectShow, vea los temas siguientes:

-   [Clases base de DirectShow](directshow-base-classes.md)
-   [Compilar filtros de DirectShow](building-directshow-filters.md)

**Crear PIN**

Un filtro debe crear uno o varios PIN. El número de clavijas se puede corregir en tiempo de diseño o el filtro puede crear nuevos PIN según sea necesario. Los pin generalmente derivan de la clase [**CBasePin**](cbasepin.md) o de una clase que hereda **CBasePin**, como [**CBaseInputPin**](cbaseinputpin.md). Los PIN del filtro se deben declarar como variables de miembro en la clase de filtro. Algunas de las clases de filtro ya definen los pin, pero si el filtro hereda directamente de **CBaseFilter**, debe declarar los pin en la clase derivada.

**Negociar conexiones de anclaje**

Cuando el administrador de gráficos de filtro intenta conectar dos filtros, los pin deben estar de acuerdo en varias cosas. Si no es así, se produce un error en el intento de conexión. Por lo general, los pin negocian lo siguiente:

-   Transport. El transporte es el mecanismo que los filtros usarán para trasladar los ejemplos de medios del PIN de salida al pin de entrada. Por ejemplo, pueden utilizar la interfaz [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) ("modelo de inserción") o la interfaz [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) ("modelo de extracción").
-   Tipo de medio. Casi todos los pin usan tipos de medios para describir el formato de los datos que van a proporcionar.
-   Asignador. El asignador es el objeto que crea los búferes que contienen los datos. Los pin deben aceptar qué PIN proporcionará el asignador. También deben estar de acuerdo en el tamaño de los búferes, el número de búferes que se van a crear y otras propiedades de búfer.

Las clases base implementan un marco para estas negociaciones. Debe completar los detalles invalidando varios métodos en la clase base. El conjunto de métodos que debe reemplazar depende de la clase y de la funcionalidad del filtro. Para obtener más información, consulte [cómo se conectan los filtros](how-filters-connect.md).

**Procesamiento y entrega de datos**

La función principal de la mayoría de los filtros es procesar y proporcionar datos multimedia. La forma en que se produce depende del tipo de filtro:

-   Un origen de la inserciones tiene un subproceso de trabajo que rellena continuamente los ejemplos con datos y los entrega de forma descendente.
-   Un origen de extracción espera a que su vecino de nivel inferior solicite un ejemplo. Responde escribiendo datos en un ejemplo y entregando el ejemplo al filtro de bajada. El filtro de nivel inferior crea el subproceso que controla el flujo de datos.
-   Un filtro de transformación tiene ejemplos que se le entregan por su vecino ascendente. Cuando recibe un ejemplo, procesa los datos y los entrega de bajada.
-   Un filtro de representador recibe ejemplos de nivel superior y los programa para su representación en función de las marcas de tiempo.

Otras tareas relacionadas con el streaming incluyen el vaciado de datos del gráfico, el control del final de la secuencia y la respuesta a las solicitudes de búsqueda. Para obtener más información acerca de estos problemas, vea los temas siguientes:

-   [Flujo de datos para desarrolladores de filtros](data-flow-for-filter-developers.md)
-   [Administración de control de calidad](quality-control-management.md)
-   [Subprocesos y secciones críticas](threads-and-critical-sections.md)

**COM compatible**

Los filtros de DirectShow son objetos COM, normalmente empaquetados en archivos dll. La biblioteca de clases base implementa un marco de trabajo para la compatibilidad con COM. Se describe en la sección [DirectShow y com](directshow-and-com.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Escribir filtros de DirectShow](writing-directshow-filters.md)
</dt> </dl>

 

 



