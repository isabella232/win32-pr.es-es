---
description: 'Más información sobre: JET_USERDEFINEDDEFAULT estructura'
title: JET_USERDEFINEDDEFAULT estructura
TOCTitle: JET_USERDEFINEDDEFAULT Structure
ms:assetid: 1f0a5419-9fae-4a93-a271-2f9772ecc996
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269200(v=EXCHG.10)
ms:contentKeyID: 32765503
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e8c34c7677a100488dfbc533aed3ca07f5b3af4c
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122988098"
---
# <a name="jet_userdefineddefault-structure"></a>JET_USERDEFINEDDEFAULT estructura


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jet_userdefineddefault-structure"></a>JET_USERDEFINEDDEFAULT estructura

La **JET_USERDEFINEDDEFAULT** estructura se especifica junto con JET_bitColumnUserDefinedDefault para proporcionar a una nueva columna un valor predeterminado que se determina mediante una devolución de llamada. Esta técnica se puede usar para implementar columnas calculadas.

**Windows XP:** La **JET_USERDEFINEDDEFAULT** se introduce en Windows XP.

```cpp
    typedef struct tag_JET_USERDEFINEDDEFAULT {
      tchar* szCallback;
      unsigned char* pbUserData;
      unsigned long cbUserData;
      tchar* szDependantColumns;
    } JET_USERDEFINEDDEFAULT;
```

### <a name="members"></a>Miembros

**szCallback**

Nombre de exportación de la función que implementa la devolución de llamada en formato "module \! function".

La devolución de llamada se conserva como parte del esquema de columna. El archivo ejecutable de host real y el nombre de exportación de la función deben conservarse para habilitar la búsqueda de la dirección verdadera de la función en tiempo de ejecución.

El nombre del módulo es el nombre del binario de host que contiene la función. El nombre de la función es el nombre de la exportación de esa función. El motor de base de datos en tiempo de ejecución usará estos dos fragmentos de información para buscar la dirección verdadera de la devolución de llamada mediante la ejecución de una llamada [LoadLibrary](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) en el nombre del módulo seguida de una llamada [GetProcAddress](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) en el nombre de la función.

Por ejemplo, si la devolución de llamada se implementó en un archivo DLL denominado MyCallback.DLL y ese archivo DLL se almacenaba en C: MyApplication y la función que implementa la devolución de llamada se exportó desde el archivo DLL como UserDefinedDefaultCallback, la cadena necesaria sería \\ "C: \\ MyApplication \\MyCallback.DLL\! UserDefinedDefaultCallback".

**Nota**  Insertado " \! " No se admiten caracteres en la parte del módulo del nombre de devolución de llamada.

Se recomienda encarecidamente usar un nombre de devolución de llamada que no sea una función de la arquitectura de host. Por ejemplo, no use exportaciones decorados como stdcall ( ) porque esta convención de llamada solo se UserDefinedDefaultCallback@32 admite en máquinas x86. Si se usaba una devolución de llamada de este tipo, la base de datos solo se podría usar en una máquina x86. En este caso, se debe usar un alias para realizar una exportación independiente de la plataforma.

Se recomienda encarecidamente usar la ruta de acceso completa del nombre del módulo que implementa la devolución de llamada. Si se usa una ruta de acceso relativa, el proceso que hospeda la base de datos podría ser susceptible a ataques por parte de un binario no fiable.

La aplicación solo debe pasar devoluciones de llamada de confianza al motor de base de datos. El motor de base de datos cargará el binario para comprobar su existencia cuando se cree la columna asociada. Si la ruta de acceso al archivo binario no se valida o se sabe que es de confianza, podría atacar el proceso que hospeda la base de datos.

**pbUserData**

Bloque independiente de datos definidos por el usuario que se pasarán a la devolución de llamada cuando se invoque. El bloque de datos que se proporciona se conservará como parte del esquema de columna. Como resultado, el bloque de datos debe ser completamente independiente y no puede hacer referencia a ningún dato que esté fuera del ámbito de la base de datos.

Si **pbUserData** es cero, se omite el valor de **cbUserData.** En este caso, no se pasará ningún dato definido por el usuario a la devolución de llamada cuando se invoque.

**cbUserData**

Vea **pbUserData**.

**szDependantColumns**

Reservado para uso futuro.

Este miembro siempre debe establecerse en NULL.

### <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 
| <p><strong>Unicode</strong></p> | <p>Se implementa como <strong>JET_ USERDEFINEDDEFAULT_W</strong> (Unicode) <strong>y JET_ USERDEFINEDDEFAULT_A</strong> (ANSI).</p> | 



### <a name="see-also"></a>Consulte también

[JET_CBTYP](./jet-cbtyp.md)  
[JET_COLUMNCREATE](./jet-columncreate-structure.md)  
[JET_COLUMNDEF](./jet-columndef-structure.md)
