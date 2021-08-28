---
description: Para los usuarios de todo el mundo, la entrada de texto forma parte de una experiencia informática moderna, para blogs, comentarios, tweets, mensajería instantánea o cualquier otro tipo de escritura de texto. En Windows 8, la revisión ortográfica está integrada para editar controles.
ms.assetid: ED569D4F-568B-4381-91C3-8EAEDA4DD47C
title: Acerca de Spell Checking API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e3c15594be003b67a6e0c9df62e234e8076cd4ea213bc08468f3bb72698f51f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119754945"
---
# <a name="about-the-spell-checking-api"></a>Acerca de Spell Checking API

Para los usuarios de todo el mundo, la entrada de texto forma parte de una experiencia informática moderna, para blogs, comentarios, tweets, mensajería instantánea o cualquier otro tipo de escritura de texto. En Windows 8, la revisión ortográfica está integrada para editar controles.

Los desarrolladores pueden usar la API de revisión ortográfica en sus aplicaciones para consumir los servicios de revisión ortográfica disponibles. Los desarrolladores también pueden crear correctores ortográficas que se convierten en proveedores y se integran en el Windows corrector ortográfica.

Spell Checking API está diseñada para su uso por parte de desarrolladores profesionales de C/C++ Windows aplicaciones del Modelo de objetos componentes (COM). Spell Checking API no se admite para su uso en un servicio Windows o ASP.NET correcto.

## <a name="versioning"></a>Control de versiones

Spell Checking API está disponible a partir de Windows 8 o Windows Server 2012. Las adiciones futuras a la API se controlarán mediante la creación de nuevas interfaces que se pueden determinar mediante [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) en las existentes.

## <a name="interfaces"></a>Interfaces

Todas las interfaces deben liberarse cuando ya no se utilicen. Todas las cadenas **LPWSTR** devueltas (parámetro out) (y los elementos **LSTRSTR** de [**IEnumString)**](/windows/win32/api/objidlbase/nn-objidlbase-ienumstring)deben liberarse con [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) cuando ya no se usen.

## <a name="error-handling"></a>Control de errores

Los errores se devuelven **como HRESULT** s. [**IErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo) e [**ISupportErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-isupporterrorinfo) no se admiten en esta API. Los errores no son especialmente útiles, excepto en el caso de argumentos incorrectos.

Cualquiera de las llamadas API puede devolver códigos de error RPC estándar porque están fuera de proceso. Se aplican tiempos de espera estándar de RPC.

## <a name="security"></a>Seguridad

Spell Checking API puede cargar código externo (proveedores de revisión ortográfica). Ejecutará este código fuera de proceso y en un contexto de seguridad restringido.

## <a name="dictionary-files"></a>Archivos de diccionario

Los diccionarios específicos del usuario para un idioma, que contiene el contenido de las listas de palabras Agregadas, Excluidas y Autocorrección, se encuentran en %AppData% Microsoft \\ \\ Spelling \\ *<language tag>* . Los nombres de archivo son default.dic (agregado), default.exc (excluido) y default.acl (AutoCorrect). Los archivos son texto no cifrado UTF-16 LE que debe comenzar con la marca de orden de bytes (BOM) adecuada. Cada línea contiene una palabra (en las listas de palabras agregadas y excluidas) o un par de autocorrección con las palabras separadas por una barra vertical (" ") (en la lista de palabras \| Autocorrección). El servicio de revisión ortográfica detectará otros archivos .dic, .exc y .acl presentes en el directorio y se agregarán a las listas de palabras del usuario. Estos archivos se consideran de solo lectura y no se modifican mediante la API de revisión ortográfica.

## <a name="installing-a-spell-checking-provider"></a>Instalación de un proveedor de revisión ortográfica

La instalación de un proveedor de revisión ortográfica debe colocar todos los archivos que usa en una ubicación que permita el acceso de lectura desde el SID[(identificador](../secauthz/security-identifiers.md)de seguridad ) "ALL APPLICATION PACKAGES". Instalarlo en una carpeta en "Archivos de programa" funciona bien. Además, el proveedor debe establecer algunas claves en el Registro para que aparezcan en la API de revisión ortográfica. Puede estar en el subárbol HKEY CURRENT USER o en el subárbol HKEY LOCAL MACHINE, en función de si debe instalarse solo para el usuario actual o \_ \_ para todos los \_ \_ usuarios.


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



El [ejemplo del proveedor de corrector](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/SpellCheckerProvider) ortográfica proporciona un ejemplo del registro necesario para instalar un proveedor.

Si va a crear nuevas opciones de revisión ortográfica para un proveedor de revisión ortográfica, consulte [**IOptionDescription::Id**](/windows/desktop/api/Spellcheck/nf-spellcheck-ioptiondescription-get_id) para obtener instrucciones sobre la nomenclatura.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de la API de revisión ortográfica](spell-checker-api-reference.md)
</dt> <dt>

[Ejemplo de cliente de revisión ortográfica](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/SpellCheckerClient)
</dt> <dt>

[Ejemplo de proveedor de revisión ortográfica](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/SpellCheckerProvider)
</dt> <dt>

[**IOptionDescription::Id**](/windows/desktop/api/Spellcheck/nf-spellcheck-ioptiondescription-get_id)
</dt> <dt>

[**IEnumString**](/windows/win32/api/objidlbase/nn-objidlbase-ienumstring)
</dt> <dt>

[**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))
</dt> </dl>

 

 
