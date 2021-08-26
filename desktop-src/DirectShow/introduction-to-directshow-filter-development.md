---
description: Introducción al desarrollo DirectShow filtros
ms.assetid: d5162ea4-ef37-4993-a82c-782f03b08c64
title: Introducción al desarrollo DirectShow filtros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2769cfe3bd4f046c117c0567104094bcad0eed730c388b551593dde6b41df25
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083695"
---
# <a name="introduction-to-directshow-filter-development"></a>Introducción al desarrollo DirectShow filtros

En esta sección se proporciona un breve esquema de las tareas implicadas en el desarrollo de un filtro DirectShow personalizado. También proporciona vínculos a temas que tratan estas tareas con más detalle. Antes de leer esta sección, lea los temas de [Acerca de DirectShow](about-directshow.md), que describen la arquitectura DirectShow general.

**DirectShow Biblioteca de clases base**

El SDK DirectShow incluye un conjunto de clases de C++ para escribir filtros. Aunque no son necesarias, estas clases son la manera recomendada de escribir un nuevo filtro. Para usar las clases base, compile en una biblioteca estática y vincule el archivo .lib al proyecto, tal y como se describe en [Building DirectShow Filters](building-directshow-filters.md).

La biblioteca de clases base define una clase raíz para los filtros, la [**clase CBaseFilter.**](cbasefilter.md) Otras clases derivan de **CBaseFilter** y están especializadas para determinados tipos de filtros. Por ejemplo, la [**clase CTransformFilter está**](ctransformfilter.md) diseñada para filtros de transformación. Para crear un nuevo filtro, implemente una clase que herede de una de las clases de filtro. Por ejemplo, la declaración de clase podría ser la siguiente:


```C++
class CMyFilter : public CTransformFilter
{
private:
    /* Declare variables and methods that are specific to your filter.
public:
    /* Override various methods in CTransformFilter */
};
```



Para obtener más información sobre las DirectShow base de datos, vea los temas siguientes:

-   [DirectShow Clases base](directshow-base-classes.md)
-   [Creación de DirectShow filtros](building-directshow-filters.md)

**Creación de pins**

Un filtro debe crear uno o varios pines. El número de pines se puede solucionar en tiempo de diseño o el filtro puede crear nuevos pines según sea necesario. Los pines suelen derivar de la [**clase CBasePin**](cbasepin.md) o de una clase que hereda **CBasePin,** como [**CBaseInputPin.**](cbaseinputpin.md) Los pines del filtro deben declararse como variables miembro en la clase de filtro. Algunas de las clases de filtro ya definen los pines, pero si el filtro hereda directamente de **CBaseFilter**, debe declarar los pines en la clase derivada.

**Negociación de conexiones de pin**

Cuando filter Graph Manager intenta conectar dos filtros, los pines deben coincidir en varias cosas. Si no es posible, se produce un error en el intento de conexión. Por lo general, los pines negocian lo siguiente:

-   Transport. El transporte es el mecanismo que usarán los filtros para mover muestras de medios desde el pin de salida al pin de entrada. Por ejemplo, pueden usar la interfaz [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) ("modelo de inserción") o la [**interfaz IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) ("modelo de extracción").
-   Tipo de medio. Casi todos los pines usan tipos de medios para describir el formato de los datos que van a entregar.
-   Asignador. El asignador es el objeto que crea los búferes que contiene los datos. Los pines deben coincidir con qué pin proporcionará el asignador. También deben coincidir en el tamaño de los búferes, el número de búferes que se van a crear y otras propiedades de búfer.

Las clases base implementan un marco para estas negociaciones. Debe completar los detalles reemplazando varios métodos de la clase base. El conjunto de métodos que debe invalidar depende de la clase y de la funcionalidad del filtro. Para obtener más información, vea [How Filters Conectar](how-filters-connect.md).

**Procesamiento y entrega de datos**

La función principal de la mayoría de los filtros es procesar y entregar datos multimedia. La forma en que se produce depende del tipo de filtro:

-   Un origen de inserción tiene un subproceso de trabajo que rellena continuamente los ejemplos con datos y los entrega de nivel inferior.
-   Un origen de extracción espera a que su vecino de nivel inferior solicite un ejemplo. Responde escribiendo datos en un ejemplo y entregando el ejemplo al filtro de nivel inferior. El filtro de nivel inferior crea el subproceso que dirige el flujo de datos.
-   Un filtro de transformación tiene ejemplos entregados por su vecino ascendente. Cuando recibe un ejemplo, procesa los datos y los entrega de nivel inferior.
-   Un filtro de representador recibe muestras de nivel superior y las programa para su representación en función de las marcas de tiempo.

Otras tareas relacionadas con el streaming incluyen vaciar los datos del gráfico, controlar el final de la secuencia y responder a las solicitudes de búsqueda. Para obtener más información sobre estos problemas, vea los temas siguientes:

-   [Datos Flow para desarrolladores de filtros](data-flow-for-filter-developers.md)
-   [Administración de control de calidad](quality-control-management.md)
-   [Subprocesos y secciones críticas](threads-and-critical-sections.md)

**Compatibilidad con COM**

DirectShow son objetos COM, normalmente empaquetados en archivos DLL. La biblioteca de clases base implementa un marco para admitir COM. Se describe en la sección DirectShow [y COM](directshow-and-com.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Escribir DirectShow filtros](writing-directshow-filters.md)
</dt> </dl>

 

 



