---
description: Modelo de objetos VDS
ms.assetid: e5fcc19a-e170-4918-85eb-c1457776795a
title: Modelo de objetos VDS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d24252facaca80fbecabdaa95c3b22f303cb864c45403ebd417d100a553dfcc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118846560"
---
# <a name="vds-object-model"></a>Modelo de objetos VDS

\[A partir Windows 8 y Windows Server 2012, la interfaz COM del servicio virtual [de](virtual-disk-service-portal.md) disco se reemplaza por [el Windows Storage API de Administración](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

VDS proporciona acceso indirecto a dispositivos de almacenamiento basados en host, como discos y dispositivos CD-ROM, y a matrices de discos administradas por controladores RAID de hardware. Mientras que algunas entidades de almacenamiento modela dispositivos físicos, otras modela construcciones virtuales: volúmenes, particiones, etc. Los objetos que se describen en este tema representan las entidades físicas y virtuales de VDS.

Las aplicaciones llaman a los métodos expuestos por estos objetos y VDS llama al proveedor adecuado para realizar las operaciones de almacenamiento solicitadas. Una aplicación nunca llama directamente a un programa de proveedor.

### <a name="classification-of-objects"></a>Clasificación de objetos

Como se muestra en la ilustración siguiente, los programas de proveedor de software implementan objetos que modela entidades basadas en host; los programas de proveedor de hardware implementan objetos que modelan dispositivos RAID de hardware internos y externos; los objetos comunes restantes son independientes del proveedor o se implementan mediante VDS. Un eje, que no es un objeto VDS, es un término para medios de almacenamiento genéricos que consta de extensiones de disco o unidad.

![Diagrama que muestra una clasificación de objetos, definida como "Objetos comunes", "Objetos de proveedor de software" y "Objetos de proveedor de hardware".](images/vdsobjectmodel.png)

Para obtener más información sobre el comportamiento de cada objeto, seleccione uno de los temas siguientes:

-   Cargador de servicios y objetos de servicio, vea [Objetos de inicio y de servicio.](startup-and-service-objects.md)
-   Enumeración y objetos asincrónicos, vea [Objetos auxiliares](helper-objects.md).
-   Objeto de proveedor, vea [Provider Object](provider-object.md).
-   Empaquetar, disco, volumen y volumen objetos plex, vea [Objetos de proveedor de software](software-provider-objects.md).
-   Subsystem, controller, drive, LUN, and LUN plex objects (Subsistema, controlador, unidad, LUN y objetos plex lun), vea [Objetos de proveedor de hardware](hardware-provider-objects.md).

### <a name="object-creation"></a>Creación de objetos

Las operaciones de configuración y consulta asociadas a la creación de objetos pueden tardar bastante tiempo en completarse. como tal, VDS invoca todos los métodos de forma asincrónica. El proveedor de devolución devuelve todos los eventos de finalización, error o cambio de estado. Los proveedores de software también registra todos los errores y cambios de estado significativos.

### <a name="object-deletion"></a>Eliminación del objeto

Varios métodos VDS eliminan o transforman objetos VDS. Un llamador puede contener una referencia, por medio de un puntero de interfaz, a un objeto eliminado después de que el método vuelva. Cuando el autor de la llamada libera la interfaz, VDS elimina el objeto.

Con respecto a la eliminación de objetos, los llamadores deben evitar invocar nada excepto el método [**IUnknown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) en estas interfaces. El proveedor debe ser lo suficientemente sólido como para tratar con llamadores errantes. Si un llamador invoca un método en un objeto eliminado, el proveedor debe devolver **VDS \_ E OBJECT \_ \_ DELETED**.

### <a name="service-initialization"></a>Inicialización del servicio

VDS proporciona un identificador de clase (Clsid) para el cargador de servicios y los objetos de servicio, pero solo el clsid del cargador de servicios es público. La inicialización del servicio se produce cuando los proveedores, una aplicación que realiza la llamada y el servicio realizan las tareas siguientes:

-   Cada nuevo proveedor invoca el [**método IVdsAdmin::RegisterProvider**](/windows/desktop/api/VdsHwPrv/nf-vdshwprv-ivdsadmin-registerprovider) durante la instalación para registrarse con VDS. La llamada crea una clave del Registro en el subárbol SYSTEM, identificado por el GUID del objeto del proveedor. Contenido en esta clave es el Clsid del objeto de proveedor, el nombre, la versión y el GUID de versión del proveedor.
    > [!Note]  
    > Los GUID de objeto de proveedor son persistentes; los GUID de objetos de hardware y software no lo son.

     

-   Una aplicación llama a la [**función CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) y pasa el clsid del cargador de servicios como argumento. Con un puntero al objeto del cargador de servicios, la aplicación puede iniciar VDS de forma local o remota pasando el nombre de equipo deseado como parámetro al método [**IVdsServiceLoader::LoadService.**](/windows/desktop/api/Vds/nf-vds-ivdsserviceloader-loadservice)
-   Cuando la aplicación inicial se asocia al servicio, VDS llama primero a [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) en cada Clsid que se encuentra en la clave del Registro y, a continuación, llama al método [**IVdsProviderPrivate::OnLoad**](/windows/desktop/api/VdsHwPrv/nf-vdshwprv-ivdsproviderprivate-onload) en cada proveedor para inicializar los programas.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de VDS](about-vds.md)
</dt> <dt>

[**IVdsAdmin::RegisterProvider**](/windows/desktop/api/VdsHwPrv/nf-vdshwprv-ivdsadmin-registerprovider)
</dt> <dt>

[**IVdsServiceLoader::LoadService**](/windows/desktop/api/Vds/nf-vds-ivdsserviceloader-loadservice)
</dt> <dt>

[**IVdsProviderPrivate::OnLoad**](/windows/desktop/api/VdsHwPrv/nf-vdshwprv-ivdsproviderprivate-onload)
</dt> </dl>

 

 
