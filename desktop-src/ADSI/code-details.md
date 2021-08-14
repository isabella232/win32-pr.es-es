---
title: Detalles del código
description: En esta sección se muestra el código fuente de la implementación del componente de proveedor de ejemplo ADSI. Todas las referencias de código fuente de este documento están sujetas a cambios y están disponibles en el directorio de código de ejemplo incluido en el SDK de ADSI.
ms.assetid: 207912e5-ac17-48c7-9536-981a8e92e8cf
ms.tgt_platform: multiple
keywords:
- ADSI de detalles del código
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0f03e7c7ed7d61d56f338a8bb44d51b1890d4bd24cd7dc1e6050f1900f6ff61
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118692291"
---
# <a name="code-details"></a>Detalles del código

En esta sección se muestra el código fuente de la implementación del componente de proveedor de ejemplo ADSI. Todas las referencias de código fuente de este documento están sujetas a cambios y están disponibles en el directorio de código de ejemplo incluido en el SDK de ADSI.

> [!Note]  
> Los [**métodos IAD**](/windows/desktop/api/Iads/nn-iads-iads) **GetEx** y **PutEx** no se implementan en el componente de proveedor de ejemplo ADSI. Es decir, el código que implementa Active Directory objetos que heredan de los **IAD no** tienen **métodos GetEx** **y PutEx.** Esto incluye el objeto de clase de esquema que admite [**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass), el objeto de propiedad que admite [**IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty), el objeto Active Directory genérico que admite los **IAD y** cualquier objeto contenedor que admita [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer). Además, los objetos de sintaxis no están presentes en el componente de proveedor de ejemplo. Sin embargo, la arquitectura ADSI requiere que los objetos de sintaxis se incluyan en el objeto contenedor de esquema, igual que los objetos de clase y propiedad de esquema.

 

En la tabla siguiente se enumeran los archivos de código fuente que se incluyen en el directorio de ejemplo del proveedor en el SDK Active Directory Service Interfaces.



| Archivo de código fuente                 | Descripción                                                                                                                                                       |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [cclsobj.cpp](cclsobj-cpp.md)   | Rutinas de objeto de clase de esquema.                                                                                                                                     |
| [cdispmgr.cpp](cdispmgr-cpp.md) | Implementación del Administrador de distribución.                                                                                                                                  |
| [cenumns.cpp](cenumns-cpp.md)   | Rutinas de enumeración de espacios de nombres.                                                                                                                                   |
| [cenumsch.cpp](cenumsch-cpp.md) | Rutinas de enumeración de esquemas.                                                                                                                                      |
| [cenumobj.cpp](cenumobj-cpp.md) | Rutinas de enumeración de objetos genéricos.                                                                                                                              |
| [cenumvar.cpp](cenumvar-cpp.md) | Implementación base para clases derivadas xxxEnumVariant.                                                                                                           |
| [cgenobj.cpp](cgenobj-cpp.md)   | Rutinas de objetos genéricos.                                                                                                                                          |
| [cnamcf.cpp](cnamcf-cpp.md)     | Rutinas de generador de clases de espacio de nombres.                                                                                                                                 |
| [cnamesp.cpp](cnamesp-cpp.md)   | Rutinas de objeto de espacio de nombres.                                                                                                                                        |
| [common.cpp](common-cpp.md)     | Código común a todos los objetos de proveedor.                                                                                                                              |
| [core.cpp](core-cpp.md)         | Implementaciones de propiedades 'core' compartidas por todos Active Directory objetos.                                                                                     |
| [cprops.cpp](cprops-cpp.md)     | Características de caché de propiedades.                                                                                                                                          |
| [cprov.cpp](cprov-cpp.md)       | Rutinas de objeto de proveedor de nivel superior.                                                                                                                               |
| [cprovcf.cpp](cprovcf-cpp.md)   | Rutinas de generador de clases de objeto de proveedor de nivel superior.                                                                                                                 |
| [cprpobj.cpp](cprpobj-cpp.md)   | Rutinas de objeto de propiedad.                                                                                                                                         |
| [cschobj.cpp](cschobj-cpp.md)   | Rutinas de objeto de esquema.                                                                                                                                           |
| [getobj.cpp](getobj-cpp.md)     | Característica GetObject.                                                                                                                                                |
| [globals.cpp](globals-cpp.md)   | Variables globales de componentes de proveedor de ejemplo adsi.                                                                                                                          |
| [guid.cpp](guid-cpp.md)         | CLID y LIBID de componentes de proveedor de ejemplo.                                                                                                                     |
| [libmain.cpp](libmain-cpp.md)   | Libmain para adssmp.dll.                                                                                                                                           |
| [memory.cpp](memory-cpp.md)     | Rutinas de administración de memoria de componentes de proveedor de ejemplo.                                                                                                            |
| [pack.cpp](pack-cpp.md)         | Ejemplo de paquete de componentes de proveedor o desempaquete de datos en variants.                                                                                                          |
| [parse.cpp](parse-cpp.md)       | Análisis de rutas de acceso, por ejemplo, espacio de nombres de componente de proveedor.                                                                                                            |
| [property.cpp](property-cpp.md) | Obtiene y coloca propiedades por nombre.                                                                                                                                   |
| [object.cpp](object-cpp.md)     | Ejemplo de código de lista de tipos de objeto de componente de proveedor para filtrar.                                                                                                   |
| [regdsapi.cpp](regdsapi-cpp.md) | API de servicio de directorio del registro de componentes de proveedor de ejemplo.                                                                                                       |
| smpoper.cpp                      | Rutinas de conversión de datos.                                                                                                                                         |
| [stdfact.cpp](stdfact-cpp.md)   | Implementación [**estándar de IClassFactory.**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory)                                                                                                  |
| adssmp.inf                       | Datos del Registro del almacén de datos de directorio de ejemplo. Para obtener más información, vea [Instalar el componente de proveedor de ejemplo](installing-the-example-provider-component.md). |



 

 

 