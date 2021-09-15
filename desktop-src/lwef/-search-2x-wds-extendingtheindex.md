---
title: Extender el índice (características heredadas Windows entorno)
description: Obtenga información sobre cómo ampliar el índice en Windows Desktop Search 2.x. Para Windows versiones posteriores a Windows XP y Windows Server 2003, use Windows Search en su lugar.
ms.assetid: vs|search|~\search\wds2x\extending_index_ovr.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63408cfe1efeb8da4d6a4540cc57b99ea56ae935
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127468797"
---
# <a name="extending-the-index-legacy-windows-environment-features"></a>Extender el índice (características heredadas Windows entorno)

> [!NOTE]
> Windows Desktop Search 2.x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003. En versiones posteriores, use [Windows Search en](../search/-search-3x-wds-overview.md) su lugar.

Se desaconseja encarecidamente el uso y el desarrollo para las versiones 2.x de Microsoft Windows Desktop Search (WDS) en favor de [Windows Search](../search/-search-3x-wds-overview.md).

WDS se puede extender para indexar el contenido de nuevos tipos de archivo y almacenes de datos. Actualmente, WDS 2.x contiene filtros para más de 200 tipos de elementos (incluidos elementos de texto no cifrado, como HTML, XML y archivos de código fuente) y usa la misma tecnología de controlador de protocolo y [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)que SharePoint Services. Si ya tiene implementaciones de filtro instaladas para los nuevos tipos de archivo, WDS puede usar las interfaces de filtro existentes para indexar estos datos.

Los complementos de WDS 2.x permiten al índice recorrer y analizar nuevas estructuras de datos y datos para obtener información que se puede agregar al catálogo en el que se pueden realizar búsquedas. Estos complementos también pueden extender el shell de Windows para asociar iconos y controladores de menú contextual con los nuevos tipos de archivo y almacenes de datos. Para incluir nuevos tipos de archivo en el catálogo de WDS, un complemento debe implementar la [**interfaz IFilter.**](/windows/desktop/api/filter/nn-filter-ifilter) Para incluir nuevos almacenes de datos, un complemento debe ser un controlador de protocolo. Si el nuevo almacén de datos incluye archivos incrustados o nuevos tipos de archivo, también tendrá que escribir un filtro adecuado.

> [!Note]
>
> Los filtros y los controladores de protocolo deben escribirse en código nativo debido a posibles problemas de control de versiones de CLR con el proceso en el que se ejecutan todos los complementos.

 

## <a name="adding-file-types-to-the-index"></a>Agregar tipos de archivo al índice

Los complementos pueden extender WDS para indexar tipos de archivo nuevos o propietarios y asociar cada nuevo tipo de archivo a un icono o menú contextual específico del archivo. Para ello, puede compilar y registrar un complemento que:

1.  Implementa una interfaz [**IFilter para**](/windows/desktop/api/filter/nn-filter-ifilter)cada tipo de archivo para que WDS pueda tener acceso al texto y los metadatos del tipo de archivo e indexarlo.
2.  Implementa las interfaces **IExtractIcon** e **IContextMenu** para agregar iconos y menús contextuales para una mayor integración y facilidad de uso.

Para obtener una explicación sobre la implementación de filtros, vea [Developing IFilter Add-ins](-search-2x-wds-ifilteraddins.md).

## <a name="adding-data-stores-to-the-index"></a>Agregar almacenes de datos al índice

Los complementos pueden extender WDS para indexar nuevos almacenes de datos y asociar archivos a un icono o menú contextual específico del archivo. Para ello, puede compilar y registrar un controlador de protocolo que:

1.  Implementa las interfaces **ISearchProtocol** **e IUrlAccessor** para procesar y enlazar elementos individuales en el origen de contenido. WDS usa direcciones URL para identificar de forma única los elementos, tanto si están en el sistema de archivos, dentro de un almacén de tipo base de datos o en la Web.
2.  Implementa la **interfaz IPersistFolder** y las partes de la interfaz **IShellFolder** para agregar iconos y menús contextuales para una mayor integración y facilidad de uso.

Para obtener una explicación sobre la implementación de controladores de protocolo, vea [Developing Protocol Handlers](-search-2x-wds-phaddins.md).

## <a name="add-in-installer-guidelines"></a>Instrucciones del instalador del complemento

La instalación de un complemento debe seguir las instrucciones siguientes:

-   El instalador debe usar el instalador EXE o MSI.
-   Se deben proporcionar notas de la versión.
-   Se **debe crear una entrada Agregar** o quitar programas para cada complemento instalado.
-   El instalador debe asumir toda la configuración del Registro para el tipo de archivo o almacén determinado que el complemento actual entiende.
-   Si se sobrescribe un complemento anterior, el instalador debe notificar al usuario.
-   Si un complemento más reciente ha sobrescrito el complemento anterior, debe haber la capacidad de restaurar la funcionalidad del complemento anterior y convertirla en el complemento predeterminado para ese tipo de archivo o almacenarlo de nuevo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Referencia**
</dt> <dt>

[Desarrollo de complementos de IFilter](-search-2x-wds-ifilteraddins.md)
</dt> <dt>

[Desarrollo de controladores de protocolo](-search-2x-wds-phaddins.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**Ifilter**](/windows/desktop/api/filter/nn-filter-ifilter)
</dt> </dl>

 

 
