---
description: Acceso al catálogo de COM+
ms.assetid: 1322a3fe-faee-4971-949f-5e0d2dfe469b
title: Acceso al catálogo de COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f05d85526cb6d82916aa48a49c7f97e581c01b7410530878a7f6e0fc69dac20
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129417"
---
# <a name="accessing-the-com-catalog"></a>Acceso al catálogo de COM+

El catálogo de COM+ es el almacén de datos subyacente que contiene todos los datos de configuración de COM+. Siempre que realice cualquier tipo de administración de COM+, leerá y escribirá los datos almacenados en el catálogo. La única manera de acceder al catálogo es a través de la herramienta administrativa Servicios de componentes o a través de la biblioteca COMAdmin.

El catálogo de COM+ proporciona una capa de abstracción sobre los detalles reales de dónde y cómo se almacenan los datos de configuración de COM+. Gran parte de los datos se almacenan en la base de datos de registro de COM+ (o RegDB), que contiene los datos de todos los componentes configurados instalados en aplicaciones COM+. Esta base de datos se usa en tiempo de ejecución de la aplicación para proporcionar datos de configuración a COM+ para activar correctamente los objetos en un contexto adecuado, lo que permite proporcionar servicios para los objetos según su configuración. El propio RegDB es un administrador de recursos con transacciones que usa transacciones DTC a través del [administrador de recursos de compensación](com--compensating-resource-manager.md); al realizar cambios de configuración persistentes, se confirman transaccionalmente. La única manera de acceder a RegDB es a través del catálogo de COM+, mediante los objetos COMAdmin o la herramienta administrativa Servicios de componentes.

En cada equipo, hay un servidor de catálogo de COM+ que se ejecuta como componente en la aplicación del sistema. El servidor de catálogo controla el acceso a los datos del catálogo almacenados en su equipo; De hecho, el servidor de catálogo es un motor de consultas que permite leer y escribir datos en el catálogo en esa máquina. Al iniciar la administración mediante programación mediante la creación de instancias de un [**objeto COMAdminCatalog,**](comadmincatalog.md) este objeto abre una sesión con el servidor de catálogo local. El servidor de catálogo local controla las solicitudes de recopilaciones o elementos de recopilación en el catálogo local. Cuando se conecta a un equipo remoto, se comunica con el servidor de catálogo en esa máquina.

## <a name="security-considerations-in-administration"></a>Consideraciones de seguridad en la administración

Para cambiar los datos en el catálogo de COM+, debe tener autoridad como administrador. Para usar la herramienta administrativa Servicios de componentes para cambiar los datos de configuración, debe ser miembro del rol Administradores asignado a la aplicación del sistema en la máquina que está intentando administrar. Del mismo modo, para cambiar los datos mediante los objetos COMAdmin, el código debe ejecutarse con autoridad de administrador. Es decir, una aplicación o script que use los objetos COMAdmin debe ejecutarse en una cuenta de usuario que esté asignada al rol Administradores en la aplicación del sistema en la máquina que está intentando administrar. La aplicación solo puede acceder a la información del catálogo y cambiarla en la medida en que la cuenta en la que se ejecuta tenga esa autoridad.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Información general de los objetos COMAdmin](overview-of-the-comadmin-objects.md)
</dt> <dt>

[Descripción resumida de las clases COMAdmin](summary-description-of-the-comadmin-classes.md)
</dt> </dl>

 

 



