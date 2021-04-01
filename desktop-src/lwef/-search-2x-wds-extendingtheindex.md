---
title: Extender el índice (características heredadas del entorno de Windows)
description: Se desaconseja encarecidamente el uso de y el desarrollo de las versiones 2. x de Microsoft Windows Desktop Search (WDS) en favor de Windows Search.
ms.assetid: vs|search|~\search\wds2x\extending_index_ovr.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ad766d6fa1c00649f7cbdc3118039ed50f13491
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104149837"
---
# <a name="extending-the-index-legacy-windows-environment-features"></a>Extender el índice (características heredadas del entorno de Windows)

> [!NOTE]
> Windows Desktop Search 2. x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003. En versiones posteriores, use la [búsqueda de Windows](../search/-search-3x-wds-overview.md) en su lugar.

Se desaconseja encarecidamente el uso de y el desarrollo de las versiones 2. x de Microsoft Windows Desktop Search (WDS) en favor de [Windows Search](../search/-search-3x-wds-overview.md).

WDS se puede extender para indizar el contenido de los nuevos tipos de archivo y almacenes de datos. Actualmente, WDS 2. x contiene filtros para más de 200 tipos de elementos (incluidos los elementos de texto no cifrado como HTML, XML y archivos de código fuente) y usa la misma tecnología de controlador de protocolo y [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)que SharePoint Services. Si ya tiene implementaciones de filtro instaladas para los nuevos tipos de archivo, WDS puede usar las interfaces de filtro existentes para indizar estos datos.

Los complementos de WDS 2. x permiten al índice atravesar y analizar nuevos datos y estructuras de datos para agregar información al catálogo de búsqueda. Estos complementos también pueden extender el shell de Windows para asociar iconos y controladores de menú contextual con los nuevos tipos de archivo y almacenes de datos. Para incluir nuevos tipos de archivo en el catálogo de WDS, un complemento debe implementar la interfaz de [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter). Para incluir nuevos almacenes de datos, un complemento debe ser un controlador de protocolo. Si el nuevo almacén de datos incluye archivos incrustados o nuevos tipos de archivo, también tendrá que escribir un filtro adecuado.

> [!Note]
>
> Los filtros y controladores de protocolo deben escribirse en código nativo debido a posibles problemas de control de versiones de CLR con el proceso en el que se ejecutan todos los complementos.

 

## <a name="adding-file-types-to-the-index"></a>Agregar tipos de archivo al índice

Los complementos pueden extender WDS para indizar tipos de archivo nuevos o propietarios y asociar cada nuevo tipo de archivo a un icono específico de archivo o menú contextual. Para ello, puede compilar y registrar un complemento que:

1.  Implementa una interfaz [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)para cada tipo de archivo, por lo que WDS puede tener acceso y indizar el texto y los metadatos del tipo de archivo.
2.  Implementa las interfaces **IExtractIcon** y **IContextMenu** para agregar iconos y menús contextuales para una mayor integración y facilidad de uso.

Para obtener una explicación sobre cómo implementar filtros, consulte [desarrollo de complementos de IFilter](-search-2x-wds-ifilteraddins.md).

## <a name="adding-data-stores-to-the-index"></a>Agregar almacenes de datos al índice

Los complementos pueden extender WDS para indexar nuevos almacenes de datos y asociar archivos con un icono específico de archivo o un menú contextual. Para ello, puede compilar y registrar un controlador de protocolo que:

1.  Implementa las interfaces **ISearchProtocol** y **IUrlAccessor** para procesar y enlazar elementos individuales en el origen de contenido. WDS usa las direcciones URL para identificar de forma única los elementos, independientemente de que estén en el sistema de archivos, dentro de un almacén similar a la base de datos o en la Web.
2.  Implementa la interfaz **IPersistFolder** y partes de la interfaz **IShellFolder** para agregar iconos y menús contextuales para una mayor integración y facilidad de uso.

Para obtener información sobre la implementación de controladores de protocolo, vea [desarrollar controladores de protocolo](-search-2x-wds-phaddins.md).

## <a name="add-in-installer-guidelines"></a>Instrucciones del instalador de complementos

La instalación de un complemento debe seguir las siguientes directrices:

-   El instalador debe utilizar el instalador EXE o MSI.
-   Se deben proporcionar las notas de la versión.
-   Se debe crear una entrada **Agregar o quitar programas** para cada complemento instalado.
-   El instalador debe asumir toda la configuración del registro para el tipo de archivo o almacén concreto que el complemento actual entienda.
-   Si se está sobrescribiendo un complemento anterior, el instalador debe notificar al usuario.
-   Si un complemento más reciente ha sobrescrito el complemento anterior, debería tener la capacidad de restaurar la funcionalidad del complemento anterior y convertirlo en el complemento predeterminado para ese tipo de archivo o para almacenarlo de nuevo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Referencia**
</dt> <dt>

[Desarrollo de complementos de IFilter](-search-2x-wds-ifilteraddins.md)
</dt> <dt>

[Desarrollar controladores de protocolo](-search-2x-wds-phaddins.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**Imaging**](/windows/desktop/api/filter/nn-filter-ifilter)
</dt> </dl>

 

 
