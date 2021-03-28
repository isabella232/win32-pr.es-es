---
description: Crea una matriz de identificadores para los iconos extraídos de un archivo especificado.
title: SHExtractIconsW función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SHExtractIconsW
- SHExtractIconsW
api_type:
- DllExport
api_location:
- Shell32.dll
ms.assetid: 9f138b4e-6a84-4c7e-9521-5f8ffe0eaebf
ms.openlocfilehash: d82eb48d45210ebf12464708b09fe469d97432db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104997769"
---
# <a name="shextracticonsw-function"></a>SHExtractIconsW función)

\[**SHExtractIconsW** está disponible a través de Windows XP Service Pack 2 (SP2). Podría modificarse o no estar disponible en versiones posteriores.\]

Crea una matriz de identificadores para los iconos extraídos de un archivo especificado.

## <a name="syntax"></a>Sintaxis


```C++
UINT SHExtractIconsW(
  _In_  LPCWSTR pszFileName,
  _In_  int     nIconIndex,
  _In_  int     cxIcon,
  _In_  int     cyIcon,
  _Out_ HICON   *phIcon,
  _Out_ UINT    *pIconId,
  _In_  UINT    nIcons,
  _In_  UINT    flags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pszFileName* \[ de\]
</dt> <dd>

Tipo: **LPCWSTR**

Puntero al nombre de archivo del que se van a extraer los iconos.

</dd> <dt>

*nIconIndex* \[ de\]
</dt> <dd>

Tipo: **int**

Índice del primer icono que se va a extraer del recurso denominado en *pszFileName*.

</dd> <dt>

*cxIcon* \[ de\]
</dt> <dd>

Tipo: **int**

Ancho deseado del icono. Vea la sección Comentarios.

</dd> <dt>

*cyIcon* \[ de\]
</dt> <dd>

Tipo: **int**

Alto deseado del icono. Vea la sección Comentarios.

</dd> <dt>

*phIcon* \[ enuncia\]
</dt> <dd>

Tipo: **HICON \** _

Cuando esta función devuelve un, contiene un puntero a la matriz de identificadores de icono.

</dd> <dt>

_pIconId * \[ out\]
</dt> <dd>

Tipo: **uint \** _

Cuando esta función vuelve, contiene un puntero al identificador de recurso del icono extraído que mejor se adapta al dispositivo de pantalla actual. Si no hay ningún identificador disponible para este formato, contiene 0xFFFFFFFF. Si no se puede obtener ningún identificador por cualquier otro motivo, devuelve cero.

</dd> <dt>

_nIcons * \[ en\]
</dt> <dd>

Tipo: **uint**

Número de iconos que se van a extraer del recurso denominado en *pszFileName*. Este parámetro solo es válido cuando el recurso es un archivo. exe o. dll.

</dd> <dt>

*marcas* \[ de de\]
</dt> <dd>

Tipo: **uint**

Marcas que controlan esta función. Para ver los valores posibles, vea el parámetro *fuLoad* de la función [**LoadImage**](/windows/win32/api/winuser/nf-winuser-loadimagea) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **uint**

Un valor distinto de cero si es correcto; de lo contrario, es cero.

## <a name="remarks"></a>Observaciones

**SHExtractIconsW** extrae de los siguientes tipos de archivo.

-   Ejecutable (.exe)
-   DLL (. dll)
-   Icono (. ico)
-   Cursor (. cur)
-   Cursor animado (. ANI)
-   Mapa de bits (.bmp)

Extracciones de Windows 3. también se admiten archivos ejecutables *de 16 bits* (. exe o. dll).

Los parámetros *cxIcon* y *cyIcon* especifican el tamaño de los iconos que se van a extraer. Se pueden extraer dos tamaños a través de cada parámetro dividiendo el valor entre su LOWORD y HIWORD. Coloque el primer tamaño deseado en el LOWORD del parámetro y el segundo tamaño en el HIWORD. Por ejemplo, [**MAKELONG**](/previous-versions/windows/desktop/legacy/ms632660(v=vs.85))(24, 48) para *cxIcon* y *cyIcon* extraen los iconos de tamaño 24 y 48.

El proceso de llamada es responsable de destruir todos los iconos extraídos mediante esta función llamando a la función [**DestroyIcon**](/windows/win32/api/winuser/nf-winuser-destroyicon) .

**SHExtractIconsW** no se exporta por nombre o se declara en un archivo de encabezado público. Para usarlo, debe declarar un prototipo coincidente y utilizar [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para solicitar un puntero de función de Shell32.dll que se pueda usar para llamar a esta función.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                          |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 5,0 o posterior)</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **SHExtractIconsW** (Unicode)<br/>                                                                      |



 

 
