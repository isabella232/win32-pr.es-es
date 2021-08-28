---
title: clave progID independiente de la versión
description: Asocia un ProgID a un CLSID. Esta clave se usa para determinar la versión más reciente de una aplicación de objeto.
ms.assetid: fb43c8d0-d923-487f-afdf-14fc29a71e0b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad09f9d86c2f34d93757e940c5262cd294485ad5
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122883145"
---
# <a name="version-independent-progid-key"></a>clave progID independiente de la versión

Asocia un ProgID a un CLSID. Esta clave se usa para determinar la versión más reciente de una aplicación de objeto.

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes
   <version-independent ProgID>
      CurVer = ProgID
```

## <a name="remarks"></a>Comentarios

La **clave HKEY \_ LOCAL MACHINE \_ SOFTWARE \\ \\ Classes** corresponde a la clave RAÍZ **HKEY \_ CLASSES, \_** que se conservaba por compatibilidad con versiones anteriores de COM.

El formato de <*progID* independiente de la versión>  es un programa <>.<componente *>,* separados por puntos, sin espacios y sin número de versión. El ProgID independiente de la versión, como ProgID, se puede registrar con un nombre legible.

*ProgID* es el ProgID de la versión instalada más reciente de la clase .

Las aplicaciones deben registrar un identificador de programación independiente de la versión en la *clave ProgID* independiente de la versión. ProgID independiente de la versión hace referencia a la clase de la aplicación y no cambia de versión a versión, sino que permanece constante en todas las versiones, por ejemplo, Microsoft Word Document. Se usa con lenguajes de macro y hace referencia a la versión instalada actualmente de la clase de la aplicación. El ProgID independiente de la versión debe corresponder al nombre de la versión más reciente de la aplicación de objeto.

Por ejemplo, el ProgID independiente de la versión se usa cuando una aplicación contenedora crea un gráfico o una tabla con un botón de barra de herramientas. En esta situación, la aplicación puede usar el ProgID independiente de la versión para determinar la versión más reciente de la aplicación de objeto necesaria.

El ProgID independiente de la versión se almacena y mantiene únicamente mediante código de aplicación. Cuando se le da el ProgID independiente de la versión, la función [**CLSIDFromProgID**](/windows/desktop/api/combaseapi/nf-combaseapi-clsidfromprogid) devuelve el CLSID de la versión actual.

Puede usar [**CLSIDFromProgID**](/windows/desktop/api/combaseapi/nf-combaseapi-clsidfromprogid) y [**ProgIDFromCLSID**](/windows/desktop/api/combaseapi/nf-combaseapi-progidfromclsid) para convertir entre estas dos representaciones.

Puede usar [**IOleObject::GetUserType**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getusertype) o [**OleRegGetUserType para**](/windows/desktop/api/Ole2/nf-ole2-olereggetusertype) cambiar el identificador a una cadena que se pueda mostrar.

Si no se usa un controlador personalizado, la entrada debe establecerse en OLE32.DLL, como se muestra en el ejemplo siguiente:

```
HKEY_CLASSES_ROOT\CLSID\{00000402-0000-0000-C000-000000000046}
   InprocHandler = ole32.dll
```

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**CLSIDFromProgID**](/windows/desktop/api/combaseapi/nf-combaseapi-clsidfromprogid)
</dt> <dt>

[**ProgIDFromCLSID**](/windows/desktop/api/combaseapi/nf-combaseapi-progidfromclsid)
</dt> <dt>

[&lt;ProgID &gt; Key](-progid--key.md)
</dt> </dl>

 

 




