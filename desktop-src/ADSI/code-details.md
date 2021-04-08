---
title: Detalles del código
description: En esta sección se muestra el código fuente de la implementación del componente de proveedor de ejemplo de ADSI. Todas las referencias del código fuente de este documento están sujetas a cambios y están disponibles en el directorio de código de ejemplo incluido en el SDK de ADSI.
ms.assetid: 207912e5-ac17-48c7-9536-981a8e92e8cf
ms.tgt_platform: multiple
keywords:
- Detalles de código ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d959357f2cdd094b26cde4f649c3286389b8415
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104078360"
---
# <a name="code-details"></a>Detalles del código

En esta sección se muestra el código fuente de la implementación del componente de proveedor de ejemplo de ADSI. Todas las referencias del código fuente de este documento están sujetas a cambios y están disponibles en el directorio de código de ejemplo incluido en el SDK de ADSI.

> [!Note]  
> Los métodos de [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) **GETEX** y **PutEx** no se implementan en el componente de proveedor de ejemplo de ADSI. Es decir, el código que implementa Active Directory objetos que heredan de **IADs** no tiene métodos **GETEX** y **PutEx** . Esto incluye el objeto de clase de esquema que admite [**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass), el objeto de propiedad que admite [**IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty), el objeto genérico Active Directory que admite **IADs** y cualquier objeto contenedor que admita [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer). Además, los objetos de sintaxis no están presentes en el componente de proveedor de ejemplo. Sin embargo, la arquitectura ADSI requiere que los objetos de sintaxis se incluyan en el objeto de contenedor de esquemas, al igual que los objetos de propiedad y de clase de esquema.

 

En la tabla siguiente se enumeran los archivos de código fuente que se incluyen en el directorio de ejemplo del proveedor en el SDK de interfaces del servicio de Active Directory.



| Archivo de código fuente                 | Descripción                                                                                                                                                       |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [cclsobj. cpp](cclsobj-cpp.md)   | Rutinas de objetos de clase de esquema.                                                                                                                                     |
| [cdispmgr. cpp](cdispmgr-cpp.md) | Implementación del administrador de distribución.                                                                                                                                  |
| [cenumns. cpp](cenumns-cpp.md)   | Rutinas de enumeración de espacios de nombres.                                                                                                                                   |
| [cenumsch. cpp](cenumsch-cpp.md) | Rutinas de enumeración de esquemas.                                                                                                                                      |
| [cenumobj. cpp](cenumobj-cpp.md) | Rutinas de enumeración de objetos genéricas.                                                                                                                              |
| [cenumvar. cpp](cenumvar-cpp.md) | Implementación base para las clases derivadas de xxxEnumVariant.                                                                                                           |
| [cgenobj. cpp](cgenobj-cpp.md)   | Rutinas de objeto genérico.                                                                                                                                          |
| [cnamcf. cpp](cnamcf-cpp.md)     | Rutinas de generador de clases de espacio de nombres.                                                                                                                                 |
| [cnamesp. cpp](cnamesp-cpp.md)   | Rutinas de objeto de espacio de nombres.                                                                                                                                        |
| [Common. cpp](common-cpp.md)     | Código común a todos los objetos de proveedor.                                                                                                                              |
| [Core. cpp](core-cpp.md)         | Implementaciones para las propiedades ' Core ' compartidas por todos los objetos de Active Directory.                                                                                     |
| [cprops. cpp](cprops-cpp.md)     | Características de caché de propiedades.                                                                                                                                          |
| [cprov. cpp](cprov-cpp.md)       | Rutinas de objeto de proveedor de nivel superior.                                                                                                                               |
| [cprovcf. cpp](cprovcf-cpp.md)   | Rutinas de generador de clases de objetos de proveedor de nivel superior.                                                                                                                 |
| [cprpobj. cpp](cprpobj-cpp.md)   | Rutinas de objeto de propiedad.                                                                                                                                         |
| [cschobj. cpp](cschobj-cpp.md)   | Rutinas de objeto de esquema.                                                                                                                                           |
| [getobj. cpp](getobj-cpp.md)     | Característica GetObject.                                                                                                                                                |
| [Globals. cpp](globals-cpp.md)   | Globales de componentes del proveedor de ejemplo de ADSI.                                                                                                                          |
| [GUID. cpp](guid-cpp.md)         | CLSID de componente de proveedor de ejemplo y LIBIDs.                                                                                                                     |
| [LibMain. cpp](libmain-cpp.md)   | LibMain para adssmp.dll.                                                                                                                                           |
| [Memory. cpp](memory-cpp.md)     | Ejemplo de rutinas de administración de memoria de componentes de proveedor.                                                                                                            |
| [Pack. cpp](pack-cpp.md)         | Paquete de componentes de proveedor de ejemplo/desempaquetar datos en variantes.                                                                                                          |
| [Parse. cpp](parse-cpp.md)       | Análisis de rutas de acceso del espacio de nombres de componentes de proveedor de ejemplo.                                                                                                            |
| [propiedad. cpp](property-cpp.md) | Obtener y colocar propiedades por nombre.                                                                                                                                   |
| [objeto. cpp](object-cpp.md)     | Ejemplo de código de tipo de objeto de componente de proveedor para filtrar.                                                                                                   |
| [regdsapi. cpp](regdsapi-cpp.md) | Ejemplo de API del servicio de directorio del registro de componentes de proveedor.                                                                                                       |
| smpoper. cpp                      | Rutinas de conversión de datos.                                                                                                                                         |
| [STDFact. cpp](stdfact-cpp.md)   | Implementación de [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) estándar.                                                                                                  |
| adssmp. inf                       | Ejemplo de datos del registro del almacén de datos de directorio. Para obtener más información, vea [instalar el componente de proveedor de ejemplo](installing-the-example-provider-component.md). |



 

 

 