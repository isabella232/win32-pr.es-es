---
description: Modelo de objetos de VDS
ms.assetid: e5fcc19a-e170-4918-85eb-c1457776795a
title: Modelo de objetos de VDS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ae998955c5d0b7834cf4d88b901537f3644a2ab
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/04/2021
ms.locfileid: "104279708"
---
# <a name="vds-object-model"></a>Modelo de objetos de VDS

\[A partir de Windows 8 y Windows Server 2012, la interfaz com de [servicio de disco virtual](virtual-disk-service-portal.md) se sustituye por la [API de administración de almacenamiento de Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

VDS proporciona acceso indirecto a los dispositivos de almacenamiento basados en host, como los discos y los dispositivos de CD-ROM, y a las matrices de discos administradas por controladores RAID de hardware. Aunque algunas entidades de almacenamiento modelan dispositivos físicos, otras construcciones virtuales de modelo: volúmenes, particiones, etc. Los objetos que se describen en este tema representan las entidades físicas y virtuales de VDS.

Las aplicaciones llaman a los métodos expuestos por estos objetos y VDS llama al proveedor adecuado para realizar las operaciones de almacenamiento solicitadas. Una aplicación nunca llama directamente a un programa de proveedor.

### <a name="classification-of-objects"></a>Clasificación de objetos

Como se muestra en la siguiente ilustración, los programas de proveedor de software implementan objetos que modelan entidades basadas en host; los programas de proveedor de hardware implementan objetos que modelan dispositivos RAID de hardware interno y externo; los objetos comunes restantes son independientes del proveedor o se implementan mediante VDS. Un eje, que no es un objeto VDS, es un término para medios de almacenamiento genéricos que constan de extensiones de disco o de unidad.

![Diagrama que muestra una clasificación de objetos, definidos como ' objetos comunes ', ' objetos de proveedor de software ' y ' objetos de proveedor de hardware '.](images/vdsobjectmodel.png)

Para obtener más información sobre el comportamiento de cada objeto, seleccione uno de los temas siguientes:

-   Los objetos de servicio y de cargador de servicio, vea [objetos de inicio y de servicio](startup-and-service-objects.md).
-   Enumeración y objetos Async, vea [objetos auxiliares](helper-objects.md).
-   Objeto de proveedor, consulte [objeto de proveedor](provider-object.md).
-   Paquetes, discos, volúmenes y objetos Plex de volumen, consulte [objetos de proveedor de software](software-provider-objects.md).
-   Subsistema, controlador, unidad, LUN y objetos de Plex LUN, consulte [objetos de proveedor de hardware](hardware-provider-objects.md).

### <a name="object-creation"></a>Creación de objetos

La configuración y las operaciones de consulta asociadas a la creación de objetos pueden tardar un tiempo considerable en completarse; como tal, VDS invoca todos los métodos de forma asincrónica. El proveedor de detección devuelve todos los eventos de finalización, error o cambio de estado. Los proveedores de software también registran todos los errores y cambios de estado significativos.

### <a name="object-deletion"></a>Eliminación del objeto

Varios métodos de VDS eliminan o transforman objetos VDS. Un llamador puede contener una referencia, por medio de un puntero de interfaz, a un objeto eliminado después de que el método devuelva. Cuando el autor de la llamada libera la interfaz, VDS elimina el objeto.

En lo que respecta a la eliminación de objetos, los autores de llamadas deberían abstenerse de invocar cualquier cosa excepto el método [**IUnknown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) en estas interfaces. El proveedor debe ser lo suficientemente sólido como para tratar con llamadores errantes; Si un llamador invoca un método en un objeto eliminado, el proveedor debe devolver el **\_ objeto VDS \_ E \_ eliminado**.

### <a name="service-initialization"></a>Inicialización del servicio

VDS proporciona un identificador de clase (CLSID) para el cargador de servicios y los objetos de servicio, pero solo el CLSID del cargador de servicios es público. La inicialización del servicio se produce cuando los proveedores, una aplicación que llama y el servicio realizan las tareas siguientes:

-   Cada proveedor nuevo invoca el método [**IVdsAdmin:: RegisterProvider**](/windows/desktop/api/VdsHwPrv/nf-vdshwprv-ivdsadmin-registerprovider) durante la instalación para registrarse con Vds. La llamada crea una clave del registro en el subárbol del sistema, identificada por el GUID del objeto del proveedor. En esta clave se incluye el CLSID del objeto de proveedor, el nombre, la versión y el GUID de la versión del proveedor.
    > [!Note]  
    > Los GUID del objeto de proveedor son persistentes; no se admiten los GUID de objetos de software y hardware.

     

-   Una aplicación llama a la función [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) y pasa el CLSID del cargador de servicios como argumento. Con un puntero al objeto de cargador de servicio, la aplicación puede iniciar VDS localmente o de forma remota pasando el nombre de equipo deseado como parámetro al método [**IVdsServiceLoader:: LoadService**](/windows/desktop/api/Vds/nf-vds-ivdsserviceloader-loadservice) .
-   Cuando la aplicación inicial se asocia al servicio, VDS llama primero a [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) en cada CLSID que se encuentra en la clave del registro y, a continuación, llama al método [**IVdsProviderPrivate:: OnLoad**](/windows/desktop/api/VdsHwPrv/nf-vdshwprv-ivdsproviderprivate-onload) en cada proveedor para inicializar los programas.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de VDS](about-vds.md)
</dt> <dt>

[**IVdsAdmin:: RegisterProvider**](/windows/desktop/api/VdsHwPrv/nf-vdshwprv-ivdsadmin-registerprovider)
</dt> <dt>

[**IVdsServiceLoader::LoadService**](/windows/desktop/api/Vds/nf-vds-ivdsserviceloader-loadservice)
</dt> <dt>

[**IVdsProviderPrivate:: OnLoad**](/windows/desktop/api/VdsHwPrv/nf-vdshwprv-ivdsproviderprivate-onload)
</dt> </dl>

 

 
