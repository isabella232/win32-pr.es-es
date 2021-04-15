---
title: Clave ProgID independiente de la versión
description: Asocia un ProgID a un CLSID. Esta clave se usa para determinar la versión más reciente de una aplicación de objeto.
ms.assetid: fb43c8d0-d923-487f-afdf-14fc29a71e0b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0a0bf379a06a6a05bb69a232ef91bb9fe81dc2f
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104488801"
---
# <a name="version-independent-progid-key"></a>Clave ProgID independiente de la versión

Asocia un ProgID a un CLSID. Esta clave se usa para determinar la versión más reciente de una aplicación de objeto.

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes
   <version-independent ProgID>
      CurVer = ProgID
```

## <a name="remarks"></a>Observaciones

La clave **HKEY \_ local \_ Machine \\ software \\ classes** corresponde a la clave **\_ \_ raíz de las clases HKEY** , que se conserva por compatibilidad con versiones anteriores de com.

El formato de <*ProgID independiente* de la versión> es <*programa*>. <*componente*>, separados por puntos, sin espacios y sin número de versión. El ProgID independiente de la versión, como el ProgID, se puede registrar con un nombre legible.

*ProgID* es el ProgID de la versión instalada más reciente de la clase.

Las aplicaciones deben registrar un identificador de programación independiente de la versión en la clave *ProgID independiente de la versión* . El ProgID independiente de la versión hace referencia a la clase de la aplicación y no cambia de la versión a la versión, sino a la constante restante en todos los versionsâ, por ejemplo, el documento de Microsoft Word. Se usa con lenguajes de macros y hace referencia a la versión instalada actualmente de la clase de la aplicación. El ProgID independiente de la versión debe corresponder al nombre de la versión más reciente de la aplicación de objeto.

Por ejemplo, el ProgID independiente de la versión se utiliza cuando una aplicación contenedora crea un gráfico o una tabla con un botón de la barra de herramientas. En esta situación, la aplicación puede usar el ProgID independiente de la versión para determinar la versión más reciente de la aplicación de objeto necesaria.

El ProgID independiente de la versión se almacena y mantiene únicamente en el código de la aplicación. Cuando se proporciona el ProgID independiente de la versión, la función [**CLSIDFromProgID**](/windows/desktop/api/combaseapi/nf-combaseapi-clsidfromprogid) devuelve el CLSID de la versión actual.

Puede usar [**CLSIDFromProgID**](/windows/desktop/api/combaseapi/nf-combaseapi-clsidfromprogid) y [**ProgIDFromCLSID**](/windows/desktop/api/combaseapi/nf-combaseapi-progidfromclsid) para realizar la conversión entre estas dos representaciones.

Puede usar [**IOleObject:: GetUserType**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getusertype) o [**OleRegGetUserType**](/windows/desktop/api/Ole2/nf-ole2-olereggetusertype) para cambiar el identificador a una cadena que se pueda mostrar.

Si no se utiliza un controlador personalizado, la entrada debe establecerse en OLE32.DLL, como se muestra en el ejemplo siguiente:

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

[<ProgID> Clave](-progid--key.md)
</dt> </dl>

 

 




