---
description: En este tema se resumen las principales consideraciones de programación que se deben tener en cuenta al agregar la funcionalidad de MUI a las aplicaciones.
ms.assetid: 10064f5c-5563-44f8-afb5-c6c77991e13c
title: Desarrollo de aplicaciones de MUI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb4a3278b4cc70969c1aa968de895d99fd3363a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912550"
---
# <a name="development-of-mui-applications"></a>Desarrollo de aplicaciones de MUI

En este tema se resumen las principales consideraciones de programación que se deben tener en cuenta al agregar la funcionalidad de MUI a las aplicaciones.

## <a name="requirements-for-a-mui-application"></a>Requisitos para una aplicación MUI

La funcionalidad de MUI se aplica solo a la localización de una aplicación totalmente globalizada, creada mediante un proceso denominado internacionalización de software. El centro para desarrolladores de Microsoft [Go global](https://msdn.microsoft.com/goglobal) proporciona una amplia variedad de documentación relacionada que le ayuda a diseñar, compilar e implementar aplicaciones de uso internacional. Estos documentos le ayudan a considerar cómo las características de distintos idiomas humanos pueden afectar al diseño del software. Tenga en cuenta que el portal también proporciona un archivo completo de las columnas Dr. International.

La aplicación MUI puede ejecutarse con cualquier idioma o configuración regional y el usuario puede solicitar cualquier idioma para el que la aplicación incluya compatibilidad. Por lo tanto, la aplicación debe codificar el texto de la interfaz de usuario para admitir la variedad más amplia posible de lenguajes. Lo más importante que debe recordar es usar [Unicode](unicode.md) para controlar todo el procesamiento de texto. Para obtener más información sobre la globalización mediante Unicode, visite el centro para desarrolladores de Microsoft [Go global](https://msdn.microsoft.com/goglobal).

## <a name="supported-programming-environments"></a>Entornos de programación admitidos

Puede Agregar la funcionalidad de MUI a una aplicación de formularios o una aplicación de consola de Win32 globalizada, tal como se describe en este SDK. Además, puede crear aplicaciones administradas mediante .NET Framework, que es compatible con MUI. Para obtener más información, vea [desarrollo de .net](/previous-versions/ff361664(v=vs.100)).

## <a name="user-interface-language-settings"></a>Configuración del idioma de la interfaz de usuario

Al planear la aplicación MUI, primero debe decidir los idiomas de la interfaz de usuario y la manera de presentarlos al usuario. La aplicación puede admitir idiomas de una de estas maneras:

-   Siga la configuración de idioma del sistema. Supongamos que los idiomas de interfaz de usuario preferidos del usuario y los idiomas de interfaz de usuario preferidos del sistema, tomados juntos, representan los idiomas disponibles para el usuario. Use el mecanismo de reserva del cargador de recursos para la selección de idioma.
-   Establecer la configuración de idioma específico de la aplicación. Admita idiomas específicos y presente un mecanismo de selección al usuario.

## <a name="resource-creation"></a>Creación de recursos

En esta sección se describen las posibilidades de crear los recursos de idioma de la interfaz de usuario para la aplicación. Para obtener más información, consulte [preparación de recursos](preparing-resources.md).

> [!Note]  
> En los sistemas operativos anteriores a Windows Vista, en general se crean aplicaciones localizadas de un solo idioma y estáticas que se pueden empaquetar de forma independiente con los idiomas admitidos por las secciones de recursos incluidas en los archivos ejecutables. Este tipo de implementación es en gran medida obsoleto y se recomienda elegir una de las otras técnicas de creación de recursos descritas en esta sección, compatible con Windows Vista y versiones posteriores. A continuación, se puede hacer que la aplicación se ejecute en sistemas operativos anteriores a Windows Vista mediante el uso de [**LoadMUILibrary**](/windows/desktop/api/Muiload/nf-muiload-loadmuilibrarya).

 

### <a name="use-of-a-single-language-in-a-resource-dll-mui-resource-technology"></a>Uso de un solo idioma en una DLL de recursos (tecnología de recursos MUI)

Muchas aplicaciones de Microsoft usan una implementación de recursos DLL satélite estándar. En este caso, se usa un archivo ejecutable principal para la aplicación MUI y se crea un archivo DLL de recursos para cada idioma admitido. El uso de un archivo DLL satélite se aplica a las aplicaciones que se ejecutan en cualquier sistema operativo Windows. Tal y como se describe en [Administración de recursos de MUI](mui-resource-management.md), la tecnología de recursos de MUI admite una variación en la implementación de dll satélite estándar.

### <a name="use-of-multiple-languages-in-a-resource-dll"></a>Uso de varios idiomas en una DLL de recursos

Puede optar por crear un archivo ejecutable principal para la aplicación MUI y un archivo DLL de recursos para los recursos asociados a los idiomas admitidos. Las copias del mismo identificador de recursos se definen en el archivo de recursos de idioma base (extensión. RC) en etiquetas de idioma diferentes para todos los idiomas admitidos.

### <a name="use-of-an-application-specific-resource-mechanism"></a>Uso de un mecanismo de recursos Application-Specific

Puede planear la aplicación MUI para que use un mecanismo de recursos personalizado. En este caso, la aplicación controla la carga de recursos de una manera especializada.

## <a name="resource-localization"></a>Localización de recursos

Para admitir los idiomas de la interfaz de usuario para la aplicación MUI, debe tener los recursos de idioma localizados. MUI admite dos tipos de localización, como se describe en la tabla siguiente.



| Tipo de localización       | Descripción                                                                                                                                                                                                                                                                |
|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Localización anterior a la compilación  | Solicite la localización antes de compilar los recursos específicos de la aplicación y del idioma. El archivo de recursos de idioma base para los idiomas de interfaz de usuario admitidos se copia y se cambia de nombre para cada idioma admitido, y las copias se proporcionan a los localizadores según sea necesario. |
| Localización posterior a la compilación | Solicite la localización después de compilar el archivo ejecutable y la DLL de recursos para la aplicación. En este caso, se proporciona una copia del archivo DLL de recursos a cada localizador.                                                                                                     |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de la interfaz de usuario multilingüe](about-multilingual-user-interface.md)
</dt> </dl>

 

 
