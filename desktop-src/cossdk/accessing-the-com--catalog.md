---
description: Obtener acceso al catálogo de COM+
ms.assetid: 1322a3fe-faee-4971-949f-5e0d2dfe469b
title: Obtener acceso al catálogo de COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f2de7c87da1744e23b384199dce68628fd77d5d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686450"
---
# <a name="accessing-the-com-catalog"></a>Obtener acceso al catálogo de COM+

El catálogo de COM+ es el almacén de datos subyacente que contiene todos los datos de configuración de COM+. Siempre que realice cualquier tipo de administración de COM+, podrá leer y escribir datos almacenados en el catálogo. La única manera de tener acceso al catálogo es a través de la herramienta administrativa Servicios de componentes o a través de la biblioteca COMAdmin.

El catálogo de COM+ proporciona una capa de abstracción sobre los detalles reales de dónde y cómo se almacenan los datos de configuración de COM+. Gran parte de los datos se almacenan en la base de datos de registro de COM+ (o RegDB), que contiene los datos de todos los componentes configurados instalados en aplicaciones COM+. Esta base de datos se utiliza en tiempo de ejecución de la aplicación para proporcionar datos de configuración a COM+ para activar correctamente los objetos en un contexto adecuado, lo que permite que se proporcionen servicios para objetos según su configuración. El propio RegDB es un administrador de recursos de transacción que usa transacciones DTC a través del [Administrador de compensación de recursos](com--compensating-resource-manager.md). Cuando se realizan cambios de configuración persistentes, se confirman de forma transaccional. La única manera de tener acceso a RegDB es a través del catálogo de COM+, mediante los objetos COMAdmin o la herramienta administrativa Servicios de componentes.

En cada equipo, hay un servidor de catálogo de COM+ que se ejecuta como un componente en la aplicación del sistema. El servidor de catálogo controla el acceso a los datos del catálogo almacenados en su equipo; en efecto, el servidor de catálogo es un motor de consultas que permite leer y escribir datos en el catálogo de ese equipo. Al iniciar la administración mediante programación creando una instancia de un objeto [**COMAdminCatalog**](comadmincatalog.md) , este objeto abre una sesión con el servidor de catálogo local. El servidor de catálogo local administra las solicitudes de recopilaciones o elementos de recopilación en el catálogo local. Cuando se conecta a un equipo remoto, se comunica con el servidor de catálogo de ese equipo.

## <a name="security-considerations-in-administration"></a>Consideraciones de seguridad en la administración

Para cambiar los datos en el catálogo de COM+, debe tener autoridad como administrador. Para usar la herramienta administrativa Servicios de componentes para cambiar los datos de configuración, debe ser miembro del rol administradores asignado a la aplicación del sistema en la máquina que está intentando administrar. Del mismo modo, para cambiar los datos mediante los objetos COMAdmin, el código debe ejecutarse con la autoridad de administrador. Es decir, una aplicación o un script con los objetos COMAdmin deben ejecutarse en una cuenta de usuario asignada al rol administradores en la aplicación del sistema en el equipo que está intentando administrar. La aplicación puede tener acceso y modificar la información del catálogo solo en la medida en que la cuenta con la que se ejecuta tiene esa autoridad.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Información general de los objetos COMAdmin](overview-of-the-comadmin-objects.md)
</dt> <dt>

[Descripción resumida de las clases COMAdmin](summary-description-of-the-comadmin-classes.md)
</dt> </dl>

 

 



