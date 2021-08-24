---
description: En este tema se resumen las consideraciones de programación principales que se deben tener en cuenta al agregar la funcionalidad DESA a las aplicaciones.
ms.assetid: 10064f5c-5563-44f8-afb5-c6c77991e13c
title: Desarrollo de aplicaciones DE LAN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32cc647069577a2ff3b137573b85308aa66e685df2310c2ea01973d19d1dc0d0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119822775"
---
# <a name="development-of-mui-applications"></a>Desarrollo de aplicaciones DE LAN

En este tema se resumen las consideraciones de programación principales que se deben tener en cuenta al agregar la funcionalidad DESA a las aplicaciones.

## <a name="requirements-for-a-mui-application"></a>Requisitos para una aplicación DE INTERFAZ DE USUARIO

La funcionalidad DESA solo se aplica a la localización de una aplicación totalmente globalizada, creada mediante un proceso denominado internacionalización de software. El Centro [para desarrolladores globales](https://msdn.microsoft.com/goglobal) de Microsoft Go proporciona una amplia selección de documentación relacionada que le ayuda a diseñar, compilar e implementar aplicaciones listas para el mundo. Estos documentos le ayudan a considerar cómo las características de los distintos lenguajes humanos pueden afectar al diseño del software. Tenga en cuenta que el portal también proporciona un archivo completo de columnas internacionales.

La aplicación DEA puede ejecutarse en cualquier idioma o configuración regional, y el usuario puede solicitar cualquier idioma para el que la aplicación incluya compatibilidad. Por lo tanto, la aplicación debe codificar el texto de la interfaz de usuario para admitir la variedad más amplia posible de idiomas. Lo más importante que se debe recordar es usar [Unicode para](unicode.md) controlar todo el procesamiento de texto. Para obtener más información sobre la globalización mediante Unicode, vea El Centro para [desarrolladores](https://msdn.microsoft.com/goglobal)globales de Microsoft Go .

## <a name="supported-programming-environments"></a>Entornos de programación admitidos

Puede agregar la funcionalidad DESA a una aplicación globalizada de formularios Win32 o a una aplicación de consola, como se describe en este SDK. Además, puede crear aplicaciones administradas mediante .NET Framework, que es compatible con LAN. Para obtener más información, vea [Desarrollo de .NET.](/previous-versions/ff361664(v=vs.100))

## <a name="user-interface-language-settings"></a>Interfaz de usuario Language Configuración

Al planear la aplicación DEA, primero debe decidir los idiomas de la interfaz de usuario y la manera de presentarlos al usuario. La aplicación puede admitir idiomas de una de estas maneras:

-   Siga la configuración del idioma del sistema. Suponga que los idiomas de interfaz de usuario preferidos por el usuario y los idiomas de interfaz de usuario preferidos del sistema, juntos, representan los idiomas disponibles para el usuario. Use el mecanismo de reserva del cargador de recursos para la selección de idioma.
-   Realice la configuración de idioma específica de la aplicación. Admite idiomas específicos y presenta un mecanismo de selección al usuario.

## <a name="resource-creation"></a>Creación de recursos

En esta sección se describen las posibilidades de crear los recursos del lenguaje de interfaz de usuario para la aplicación. Para obtener más información, vea [Preparar recursos.](preparing-resources.md)

> [!Note]  
> En los sistemas operativos Windows Vista, normalmente se crean aplicaciones estáticas y empaquetadas por separado localizadas de un solo idioma con los idiomas admitidos por las secciones de recursos incluidas en los archivos ejecutables. Este tipo de implementación está obsoleto en gran medida y se recomienda elegir una de las otras técnicas de creación de recursos que se describen en esta sección, compatible con Windows Vista y versiones posteriores. A continuación, se puede hacer que la aplicación se ejecute en sistemas operativos Windows Vista mediante el uso [**de LoadMUILibrary**](/windows/desktop/api/Muiload/nf-muiload-loadmuilibrarya).

 

### <a name="use-of-a-single-language-in-a-resource-dll-mui-resource-technology"></a>Uso de un solo lenguaje en un archivo DLL de recursos (tecnología de recursos DE LAN)

Muchas aplicaciones de Microsoft usan una implementación estándar de recursos DLL satélite. En este caso, se usa un archivo ejecutable principal para la aplicación DE JAVA y se crea un archivo DLL de recursos para cada lenguaje compatible. El uso de un archivo DLL satélite se aplica a las aplicaciones que se ejecutan en cualquier Windows operativo. Como se describe en [Administración de recursos DE LAN,](mui-resource-management.md)la tecnología de recursos DE LAN admite una variación en la implementación estándar de DLL satélite.

### <a name="use-of-multiple-languages-in-a-resource-dll"></a>Uso de varios idiomas en un archivo DLL de recursos

Puede optar por crear un archivo ejecutable principal para la aplicación DE JAVA y un archivo DLL de recursos para los recursos asociados a los idiomas admitidos. Las copias del mismo identificador de recursos se definen en el archivo de recursos de lenguaje base (extensión .rc) en etiquetas de idioma diferentes para todos los idiomas admitidos.

### <a name="use-of-an-application-specific-resource-mechanism"></a>Uso de un mecanismo Application-Specific recursos

Puede planear la aplicación DE AME para usar un mecanismo de recursos personalizado. En este caso, la aplicación controla su carga de recursos de forma especializada.

## <a name="resource-localization"></a>Localización de recursos

Para admitir los idiomas de la interfaz de usuario para la aplicación DEA, debe tener localizados los recursos de idioma. LA INTERFAZ de usuario admite dos tipos de localización, como se describe en la tabla siguiente.



| Tipo de localización       | Descripción                                                                                                                                                                                                                                                                |
|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Localización previa a la compilación  | Solicite localización antes de compilar la aplicación y los recursos específicos del lenguaje. El archivo de recursos de idioma base para los idiomas de interfaz de usuario admitidos se copia y cambia de nombre para cada idioma admitido, y las copias se proporcionan a los localizadores según sea necesario. |
| Localización posterior a la compilación | Solicite localización después de compilar el archivo ejecutable y el archivo DLL de recursos para la aplicación. En este caso, se proporciona una copia del archivo DLL de recursos a cada localizador.                                                                                                     |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de Interfaz de usuario multilingüe](about-multilingual-user-interface.md)
</dt> </dl>

 

 
