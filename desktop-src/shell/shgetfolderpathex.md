---
UID: ''
title: SHGetFolderPathEx función)
description: Recupera la ruta de acceso de una carpeta conocida identificada por KNOWNFOLDERID.
old-location: ''
ms.assetid: na
ms.date: 04/10/2019
ms.keywords: SHGetFolderPath
ms.topic: reference
req.header: Shlobj.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: Shell32.lib
req.dll: API-MS-Win-Storage-Exports-Internal-L1-1-0.dll
req.irql: ''
topic_type:
- APIRef
api_type: ''
api_location:
- API-MS-Win-Storage-Exports-Internal-L1-1-0.dll
api_name:
- SHGetFolderPathEx
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: 0dfc3342f3eca5622c25d2df7319cd2323f516ff
ms.sourcegitcommit: 1f6a1bfc1c4bb2641bc3ba44beb1f2727c94681b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2020
ms.locfileid: "104983947"
---
# <a name="shgetfolderpathex-function"></a>SHGetFolderPathEx función)

## <a name="description"></a>Descripción

\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.
Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]

Recupera la ruta de acceso completa de una carpeta conocida identificada por el [KNOWNFOLDERID](/windows/desktop/shell/knownfolderid)de la carpeta.
Esto extiende [SHGetKnownFolderPath](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) permitiendo establecer el tamaño inicial del búfer de cadena.

```cpp
HRESULT WINAPI SHGetFolderPathEx(
  _In_     REFKNOWNFOLDERID rfid,
  _In_     DWORD            dwFlags,
  _In_opt_ HANDLE           hToken,
  _Out_    LPWSTR           pszPath,
  _In_     UINT             cchPath
);
```

## <a name="parameters"></a>Parámetros

### <a name="rfid-in"></a>RFID [in]

Referencia a **KNOWNFOLDERID** que identifica la carpeta.

### <a name="dwflags-in"></a>dwFlags [in]

Marcas que especifican opciones de recuperación especiales.
Este valor puede ser 0; de lo contrario, uno o varios de los valores de [KNOWN_FOLDER_FLAG](/windows/desktop/api/shlobj_core/ne-shlobj_core-known_folder_flag) .

### <a name="htoken-in-optional"></a>hToken [in, Optional]

Un [token de acceso](/windows/desktop/SecAuthZ/access-tokens) que representa a un usuario determinado.
Si este parámetro es **null**, que es el uso más común, la función solicita la carpeta conocida para el usuario actual.

Solicite una carpeta de usuario específica pasando el *hToken* de ese usuario.
Esto se hace normalmente en el contexto de un servicio que tiene privilegios suficientes para recuperar el token de un usuario determinado.
Dicho token debe abrirse con derechos [TOKEN_QUERY](/windows/desktop/SecAuthZ/access-rights-for-access-token-objects) y [TOKEN_IMPERSONATE](/windows/desktop/SecAuthZ/access-rights-for-access-token-objects) .
En algunos casos, también debe incluir [TOKEN_DUPLICATE](/windows/desktop/SecAuthZ/access-rights-for-access-token-objects).
Además de pasar el *hToken* del usuario, se debe montar el subárbol del registro de ese usuario específico.
Consulte [Access Control](/windows/desktop/SecAuthZ/access-control) para obtener más información sobre los problemas de control de acceso.

Al asignar el parámetro *hToken* un valor de-1, se indica el usuario predeterminado.
Esto permite a los clientes de [SHGetKnownFolderPath](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) buscar ubicaciones de carpetas (por ejemplo, la carpeta **escritorio** ) del usuario predeterminado.
El perfil de usuario de usuario predeterminado se duplica cuando se crea una cuenta de usuario nueva e incluye carpetas especiales como **documentos** y **escritorio**.
Los elementos agregados a la carpeta de usuario predeterminada también aparecen en cualquier cuenta de usuario nueva.
Tenga en cuenta que el acceso a las carpetas de usuario predeterminadas requiere privilegios de administrador.

### <a name="pszpath-out"></a>pszPath [out]

Una cadena Unicode terminada en NULL.
Este búfer debe tener el tamaño cchPath.
Cuando **SHGetFolderPathEx** se devuelve correctamente, este parámetro contiene la ruta de acceso de la carpeta conocida.

### <a name="cchpath-in"></a>cchPath [in]

Tamaño del búfer de *ppszPath* , en caracteres.

## <a name="returns"></a>Devoluciones

Devuelve **S_OK** si se realiza correctamente, o un valor de error en caso contrario.

## <a name="remarks"></a>Observaciones

Como [SHGetFolderPath](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) es un contenedor para [SHGetKnownFolderPath](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath), esta función (**SHGetFolderPathEx**) también sirve como extensión a **SHGetFolderPath**.

## <a name="see-also"></a>Vea también

[KNOWNFOLDERID](/windows/desktop/shell/knownfolderid)

[KNOWN_FOLDER_FLAG](/windows/desktop/api/shlobj_core/ne-shlobj_core-known_folder_flag)

[SHGetFolderPath](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha)

[SHGetKnownFolderIDList](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderidlist)

[SHGetKnownFolderPath](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath)
