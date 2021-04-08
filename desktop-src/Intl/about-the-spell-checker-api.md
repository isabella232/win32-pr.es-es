---
description: Para los usuarios de todo el mundo, la entrada de texto es parte de una experiencia informática moderna, para blogs, comentarios, tweets, mensajería instantánea o cualquier otro tipo de escritura de texto. En Windows 8, la revisión ortográfica está integrada en los controles de edición.
ms.assetid: ED569D4F-568B-4381-91C3-8EAEDA4DD47C
title: Acerca de la API de revisión ortográfica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f0d356823e665781052e2a2d5ea98b358155038
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910993"
---
# <a name="about-the-spell-checking-api"></a>Acerca de la API de revisión ortográfica

Para los usuarios de todo el mundo, la entrada de texto es parte de una experiencia informática moderna, para blogs, comentarios, tweets, mensajería instantánea o cualquier otro tipo de escritura de texto. En Windows 8, la revisión ortográfica está integrada en los controles de edición.

Los desarrolladores pueden usar la API de revisión ortográfica en sus aplicaciones para consumir los servicios de revisión ortográfica disponibles. Los desarrolladores también pueden crear comprobadores ortográficos que se convierten en proveedores y se integran en el marco de revisión ortográfica de Windows.

La API de revisión ortográfica está diseñada para que la usen los desarrolladores profesionales de C/C++ de las aplicaciones de modelo de objetos componentes (COM) de Windows. No se admite el uso de la API de revisión ortográfica en un servicio de Windows o ASP.NET.

## <a name="versioning"></a>Control de versiones

La API de revisión ortográfica está disponible a partir de Windows 8 o Windows Server 2012. Las futuras adiciones a la API se controlarán mediante la creación de nuevas interfaces que se pueden determinar mediante [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) en las existentes.

## <a name="interfaces"></a>Interfaces

Todas las interfaces deben liberarse cuando ya no se usen. Todas **las cadenas (** y los elementos **LPOLESTR** de [**IEnumString**](/windows/win32/api/objidlbase/nn-objidlbase-ienumstring)) devueltas (parámetro out) deben liberarse con [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) cuando ya no se usen.

## <a name="error-handling"></a>Control de errores

Los errores se devuelven como **HRESULT** s. [**IErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo) y [**ISupportErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-isupporterrorinfo) no se admiten en esta API. Los errores no son especialmente accionables salvo los argumentos incorrectos.

Los códigos de error RPC estándar pueden ser devueltos por cualquiera de las llamadas a la API porque son fuera de proceso. Se aplican los tiempos de espera de RPC estándar.

## <a name="security"></a>Seguridad

La API de revisión ortográfica puede cargar código externo (proveedores de corrector ortográfico). Este código se ejecutará fuera de proceso y en un contexto de seguridad restringido.

## <a name="dictionary-files"></a>Archivos de Diccionario

Los diccionarios específicos del usuario para un idioma, que contienen el contenido de las listas de palabras agregadas, excluidas y de Autocorrección, se encuentran en% AppData% \\ Microsoft \\ Spelling \\ *<language tag>* . Los nombres de archivo son default. dic (agregado), default. exc (Excluded) y default. ACL (Autocorrección). Los archivos son texto sin formato UTF-16 LE que debe comenzar con la marca de orden de bytes (BOM) adecuada. Cada línea contiene una palabra (en las listas de palabras agregadas y excluidas) o un par de Autocorrección con las palabras separadas por una barra vertical (" \| ") (en la lista de palabras de Autocorrección). Otros archivos. dic,. exc y. ACL presentes en el directorio serán detectados por el servicio de revisión ortográfica y agregados a las listas de palabras de usuario. Estos archivos se consideran de solo lectura y no se modifican mediante la API de revisión ortográfica.

## <a name="installing-a-spell-checking-provider"></a>Instalación de un proveedor de revisión ortográfica

La instalación de un proveedor de revisión ortográfica debe colocar todos los archivos que utiliza en una ubicación que permita el acceso de lectura desde el SID ([identificador de seguridad](../secauthz/security-identifiers.md)) "todos los paquetes de aplicación". Instalarlo en una carpeta en "archivos de programa" funciona bien. Además, el proveedor debe establecer algunas claves en el registro para que aparezcan en la API de revisión ortográfica. Puede estar en el subárbol del \_ usuario actual HKEY \_ o en el \_ \_ subárbol del equipo local HKEY, en función de si debe instalarse solo para el usuario actual o para todos los usuarios.


```
Key: <Registry hive>\SOFTWARE\Classes\CLSID\<Server CLSID>
     Default (REG_SZ) = <Name of the provider>

Key: <Registry hive>\SOFTWARE\Classes\CLSID\<Server CLSID>\InprocServer32
     ThreadingModel (REG_SZ) = "Both"

Key: <Registry hive>\SOFTWARE\Classes\CLSID\<Server CLSID>\Version
     Version (REG_SZ) = <Version>

Key: <Registry hive>\SOFTWARE\Microsoft\Spelling\Spellers\<Provider id string>
     CLSID (REG_SZ) = <CLSID of the COM Server that implements the provider>
```



El [ejemplo de proveedor](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/SpellCheckerProvider) de revisión ortográfica proporciona un ejemplo del registro necesario para instalar un proveedor.

Si va a crear nuevas opciones de revisión ortográfica para un proveedor de revisión ortográfica, consulte [**IOptionDescription:: ID**](/windows/desktop/api/Spellcheck/nf-spellcheck-ioptiondescription-get_id) para obtener instrucciones sobre la nomenclatura.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de la API de revisión ortográfica](spell-checker-api-reference.md)
</dt> <dt>

[Ejemplo de cliente de revisión ortográfica](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/SpellCheckerClient)
</dt> <dt>

[Ejemplo de proveedor de revisión ortográfica](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/SpellCheckerProvider)
</dt> <dt>

[**IOptionDescription:: ID**](/windows/desktop/api/Spellcheck/nf-spellcheck-ioptiondescription-get_id)
</dt> <dt>

[**IEnumString**](/windows/win32/api/objidlbase/nn-objidlbase-ienumstring)
</dt> <dt>

[**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))
</dt> </dl>

 

 
