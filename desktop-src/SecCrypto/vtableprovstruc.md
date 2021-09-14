---
description: Contiene punteros a funciones de devolución de llamada que pueden usar las funciones del proveedor de servicios criptográficos (CSP).
ms.assetid: 84a379e9-c6b9-4c1d-bbbb-9bed4a045d90
title: Estructura VTableProvStruc (Cspdk.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- VTableProvStruc
- VTableProvStrucW
api_type:
- HeaderDef
api_location:
- Cspdk.h
ms.openlocfilehash: 99b9344c6951dc93972315d9b4f60752f1484d68
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127170829"
---
# <a name="vtableprovstruc-structure"></a>Estructura VTableProvStruc

La **estructura VTableProvStruc** contiene punteros a funciones de devolución de llamada que pueden usar las funciones [*del*](../secgloss/c-gly.md) proveedor de servicios criptográficos (CSP).

## <a name="syntax"></a>Sintaxis


```C++
typedef struct VTableProvStruc {
  DWORD   Version;
  FARPROC FuncVerifyImage;
  FARPROC FuncReturnhWnd;
  DWORD   dwProvType;
  BYTE    *pbContextInfo;
  DWORD   cbContextInfo;
  LPSTR   pszProvName;
} VTableProvStruc, *PVTableProvStruc;
```



## <a name="members"></a>Members

<dl> <dt>

**Versión**
</dt> <dd>

Valor **DWORD** que indica la versión de la estructura. Se usan tres versiones de esta estructura. Las versiones son el número 1, 2 y 3 y determinan qué miembros de la estructura son válidos. Los miembros de la versión 1 son válidos en todos los sistemas que admiten esta estructura.

Se trata de un miembro de la versión 1.

</dd> <dt>

**FuncVerifyImage**
</dt> <dd>

Dirección de una función de devolución de llamada [**FuncVerifyImage**](funcverifyimage.md) que el CSP usa para comprobar la firma de los archivos DLL que el CSP cargará. Todos los archivos DLL auxiliares en los que un CSP realiza llamadas a funciones deben estar firmados de la misma manera (y con la misma clave) que el archivo DLL de CSP principal. Para garantizar esta firma, los archivos DLL auxiliares se deben cargar dinámicamente mediante la [**función LoadLibrary.**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) Pero antes de cargar el archivo DLL, se debe comprobar la firma del archivo DLL. El CSP realiza esta comprobación mediante una llamada a la **función FuncVerifyImage,** como se muestra en el ejemplo siguiente.

Este puntero de función se puede almacenar y usar hasta que se libera el contexto de CSP.

Se trata de un miembro de la versión 1.

</dd> <dt>

**FuncReturnhWnd**
</dt> <dd>

Dirección de una función de devolución de llamada [**FuncReturnhWnd**](funcreturnhwnd.md) que devuelve el identificador de ventana que el CSP debe usar como el elemento primario o propietario de cualquier interfaz de usuario que se muestre. Los CSP que no se comunican directamente con el usuario y los CSP que usan hardware dedicado para este propósito pueden omitir esta entrada. Este identificador de ventana es cero de forma predeterminada, pero una aplicación puede establecerlo en un valor diferente mediante la función [**CryptSetProvParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetprovparam) para establecer la propiedad **\_ \_ HWND** del cliente de PP.

Este puntero de función se puede almacenar y usar hasta que se libera el contexto de CSP.

Se trata de un miembro de la versión 1.

</dd> <dt>

**dwProvType**
</dt> <dd>

Valor **DWORD** que especifica el tipo de proveedor que se debe adquirir. Los siguientes [*tipos de proveedor*](../secgloss/p-gly.md) están predefinidos y se analizan en detalle en [Interoperabilidad de CSP:](https://www.bing.com/search?q=CSP+Interoperability)

-   PROV \_ RSA \_ FULL
-   PROV \_ RSA \_ SIG
-   PROV \_ DSS
-   PROV \_ FORTEZZA
-   PROV \_ MS \_ EXCHANGE

Se trata de un miembro de la versión 2.

</dd> <dt>

**pbContextInfo**
</dt> <dd>

Puntero a una matriz de información de contexto. Los **miembros pbContextInfo** y **cbContextInfo** juntos determinan el conjunto de información utilizado cuando se llama a una función [**CPSetProvParam**](https://www.bing.com/search?q=**CPSetProvParam**) con el conjunto DE INFORMACIÓN \_ DE CONTEXTO DE \_ PP.

Se trata de un miembro de la versión 2.

</dd> <dt>

**cbContextInfo**
</dt> <dd>

Valor **DWORD** que indica el número de elementos de la **matriz pbContextInfo.**

Se trata de un miembro de la versión 2.

</dd> <dt>

**pszProvName**
</dt> <dd>

Cadena que contiene el nombre del proveedor.

Se trata de un miembro de la versión 3.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Los punteros de la **estructura VTableProvStruc** solo están disponibles dentro de la [**función CPAcquireContext.**](https://www.bing.com/search?q=**CPAcquireContext**) Si se necesitan miembros de la estructura una vez completada una llamada a **CPAcquireContext,** el CSP debe realizar copias de los elementos de estructura necesarios. Los punteros de función de esta estructura se pueden almacenar y usar hasta que se libera el contexto de CSP.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Cspdk.h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **VTableProvStrucW** (Unicode)<br/>                                          |



 

 
