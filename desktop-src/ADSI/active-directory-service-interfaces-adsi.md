---
title: Interfaces de servicio de Active Directory
description: Introducción a las interfaces de Active Directory Services, con vínculos a diferentes guías.
ms.assetid: b24f9789-b9f5-49c4-9812-298bae8b28a9
ms.tgt_platform: multiple
keywords:
- ADSI ADSI
- Interfaces de servicio Active Directory (consulte ADSI)
- ADSI ADSI, página de inicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15cc702fec86f1202f1fbd00ba575fd848e4ab74
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104078367"
---
# <a name="active-directory-service-interfaces"></a>Interfaces de servicio de Active Directory

## <a name="purpose"></a>Propósito

Active Directory interfaces de servicio (ADSI) es un conjunto de interfaces COM que se usan para tener acceso a las características de los servicios de directorio de proveedores de red diferentes. ADSI se usa en un entorno informático distribuido para presentar un único conjunto de interfaces de servicios de directorio para administrar los recursos de red. Los administradores y programadores pueden usar los servicios ADSI para enumerar y administrar los recursos de un servicio de directorio, independientemente del entorno de red que contenga el recurso.

ADSI permite realizar tareas administrativas comunes, como agregar nuevos usuarios, administrar impresoras y buscar recursos en un entorno de computación distribuida.

> [!Note]  
> La siguiente documentación es para programadores de equipos. Si es un usuario final que está intentando depurar un error de impresión o un problema de la red doméstica, consulte los foros de la [comunidad de Microsoft](https://answers.microsoft.com).

 

## <a name="where-applicable"></a>Donde sea aplicable

Los administradores de red pueden usar ADSI para automatizar tareas comunes, como agregar usuarios y grupos, administrar impresoras y establecer permisos en los recursos de red.

Los fabricantes de software independientes y los desarrolladores de usuarios finales pueden usar ADSI para "habilitar el directorio" sus productos y aplicaciones. Los servicios pueden publicarse en un directorio, los clientes pueden usar el directorio para encontrar los servicios y ambos pueden usar el directorio para buscar y manipular otros objetos de interés. Dado que Active Directory interfaces de servicio son independientes de los servicios de directorio subyacentes, los productos y las aplicaciones habilitadas para el directorio pueden funcionar correctamente en varios entornos de red y de directorio.

## <a name="developer-audience"></a>Audiencia de desarrolladores

Puede escribir aplicaciones cliente ADSI en muchos idiomas. Para la mayoría de las tareas administrativas, ADSI define interfaces y objetos a los que se puede acceder desde lenguajes compatibles con la automatización, como Microsoft Visual Basic, Microsoft Visual Basic Scripting Edition (VBScript) y Java, a los lenguajes más conscientes del rendimiento y la eficacia, como C y C++. Una buena base en la programación COM es útil para el programador de ADSI.

## <a name="run-time-requirements"></a>Requisitos de tiempo de ejecución

Active Directory se ejecuta en controladores de dominio de Windows Server. Sin embargo, las aplicaciones cliente que usan ADSI pueden escribirse y ejecutarse en Windows. Además, los desarrolladores querrán el kit de desarrollo de software (SDK) de la plataforma, que también está disponible en el sitio web de MSDN. Para investigar el contenido de Active Directory, utilice el complemento MMC usuarios y equipos Active Directory. Este complemento reemplaza a la herramienta Adsvw que estaba disponible para versiones anteriores de Windows.

## <a name="in-this-section"></a>En esta sección

<dl> <dt>

[Acerca de ADSI](about-adsi.md)
</dt> <dd>

Información general acerca de ADSI.

</dd> <dt>

[Usar ADSI](using-adsi.md)
</dt> <dd>

Guía del programador sobre el uso de ADSI.

</dd> <dt>

[Tutoriales de inicio rápido de ADSI](adsi-quick-start-tutorials.md)
</dt> <dd>

Usar ADSI con automatización para administrar directorios.

</dd> <dt>

[Referencia ADSI](adsi-reference.md)
</dt> <dd>

Documentación de los métodos y las interfaces ADSI.

</dd> </dl>

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[The Component Object Model](../com/the-component-object-model.md) [Modelo de objetos componentes (COM)]
</dt> <dt>

[Clientes y servidores COM](../com/com-clients-and-servers.md)
</dt> <dt>

[Active Directory Domain Services](../ad/active-directory-domain-services.md)
</dt> </dl>

 

 