---
description: Contiene punteros a funciones de devolución de llamada que pueden usar las funciones del proveedor de servicios criptográficos (CSP).
ms.assetid: 84a379e9-c6b9-4c1d-bbbb-9bed4a045d90
title: Estructura VTableProvStruc (Cspdk. h)
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103817635"
---
# <a name="vtableprovstruc-structure"></a>Estructura VTableProvStruc

La estructura **VTableProvStruc** contiene punteros a funciones de devolución de llamada que pueden usar las funciones del [*proveedor de servicios criptográficos*](../secgloss/c-gly.md) (CSP).

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



## <a name="members"></a>Miembros

<dl> <dt>

**Versión**
</dt> <dd>

Valor **DWORD** que indica la versión de la estructura. Se usan tres versiones de esta estructura. Las versiones son los números 1, 2 y 3, y determinan qué miembros de la estructura son válidos. Los miembros de la versión 1 son válidos en todos los sistemas que admiten esta estructura.

Se trata de un miembro de la versión 1.

</dd> <dt>

**FuncVerifyImage**
</dt> <dd>

La dirección de una función de devolución de llamada [**FuncVerifyImage**](funcverifyimage.md) que usa el CSP para comprobar la firma de los archivos DLL que el CSP va a cargar. Todas las DLL auxiliares en las que un CSP realiza llamadas a funciones deben estar firmadas de la misma manera (y con la misma clave) que la DLL de CSP principal. Para garantizar esta firma, los archivos dll auxiliares se deben cargar dinámicamente mediante la función [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) . Pero antes de que se cargue el archivo DLL, se debe comprobar la firma de la DLL. El CSP realiza esta comprobación mediante una llamada a la función **FuncVerifyImage** , tal como se muestra en el ejemplo siguiente.

Este puntero de función se puede almacenar y usar hasta que se libere el contexto CSP.

Se trata de un miembro de la versión 1.

</dd> <dt>

**FuncReturnhWnd**
</dt> <dd>

La dirección de una función de devolución de llamada [**FuncReturnhWnd**](funcreturnhwnd.md) que devuelve el identificador de ventana que el CSP debe utilizar como elemento primario o propietario de cualquier interfaz de usuario que se muestre. Los CSP que no se comunican directamente con el usuario y los CSP que usan Hardware dedicado para este propósito pueden omitir esta entrada. De forma predeterminada, este identificador de ventana es cero, pero una aplicación puede establecerlo en un valor diferente mediante la función [**CryptSetProvParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetprovparam) para establecer la propiedad **\_ \_ hWnd del cliente PP** .

Este puntero de función se puede almacenar y usar hasta que se libere el contexto CSP.

Se trata de un miembro de la versión 1.

</dd> <dt>

**dwProvType**
</dt> <dd>

Valor **DWORD** que especifica el tipo de proveedor que se va a adquirir. Los siguientes [*tipos de proveedor*](../secgloss/p-gly.md) están predefinidos y se describen en detalle en [interoperabilidad de CSP](https://www.bing.com/search?q=CSP+Interoperability):

-   aprovisionamiento \_ completo de RSA \_
-   \_firma RSA \_ SIG
-   DSS de PROV \_
-   Fortezza de PROV \_
-   \_Microsoft \_ Exchange

Este es un miembro de la versión 2.

</dd> <dt>

**pbContextInfo**
</dt> <dd>

Puntero a una matriz de información de contexto. Juntos, los miembros **pbContextInfo** y **cbContextInfo** determinan el conjunto de información que se usa cuando se llama a una función [**CPSetProvParam**](https://www.bing.com/search?q=**CPSetProvParam**) con la información de contexto de PP \_ \_ establecida.

Este es un miembro de la versión 2.

</dd> <dt>

**cbContextInfo**
</dt> <dd>

Valor **DWORD** que indica el número de elementos de la matriz **pbContextInfo** .

Este es un miembro de la versión 2.

</dd> <dt>

**pszProvName**
</dt> <dd>

Cadena que contiene el nombre del proveedor.

Se trata de un miembro de la versión 3.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Los punteros de la estructura **VTableProvStruc** solo están disponibles dentro de la función [**CPAcquireContext**](https://www.bing.com/search?q=**CPAcquireContext**) . Si los miembros de la estructura son necesarios después de que se complete una llamada a **CPAcquireContext** , el CSP debe realizar copias de los elementos de la estructura necesarios. Los punteros de función de esta estructura se pueden almacenar y usar hasta que se libere el contexto CSP.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Cspdk. h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **VTableProvStrucW** (Unicode)<br/>                                          |



 

 
