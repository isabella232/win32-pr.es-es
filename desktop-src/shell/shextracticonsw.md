---
description: Crea una matriz de identificadores para los iconos extraídos de un archivo especificado.
title: Función SHExtractIconsW
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
ms.openlocfilehash: 699b6d5473d97548a22e220372b9f53633cb2346
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2021
ms.locfileid: "109840916"
---
# <a name="shextracticonsw-function"></a>Función SHExtractIconsW

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

*pszFileName* \[ En\]
</dt> <dd>

Tipo: **LPCWSTR**

Puntero al nombre de archivo del que se extraen los iconos.

</dd> <dt>

*nIconIndex* \[ En\]
</dt> <dd>

Tipo: **int**

Índice del primer icono que se extraerá del recurso denominado *en pszFileName*.

</dd> <dt>

*cxIcon* \[ En\]
</dt> <dd>

Tipo: **int**

Ancho deseado del icono. Vea la sección Comentarios.

</dd> <dt>

*cyIcon* \[ En\]
</dt> <dd>

Tipo: **int**

Alto deseado del icono. Vea la sección Comentarios.

</dd> <dt>

*phIcon* \[ out\]
</dt> <dd>

Tipo: **HICON \***

Cuando esta función devuelve un resultado, contiene un puntero a la matriz de identificadores de icono.

</dd> <dt>

*pIconId* \[ out\]
</dt> <dd>

Tipo: **UINT \***

Cuando esta función vuelve, contiene un puntero al identificador de recursos del icono extraído que mejor se adapta al dispositivo de visualización actual. Si no hay ningún identificador disponible para este formato, contiene 0xFFFFFFFF. Si no se puede obtener ningún identificador por cualquier otro motivo, devuelve cero.

</dd> <dt>

*nIcons* \[ En\]
</dt> <dd>

Tipo: **UINT**

Número de iconos que se extraerán del recurso denominado *en pszFileName.* Este parámetro solo es válido cuando el recurso es un archivo .exe o .dll.

</dd> <dt>

*flags* \[ En\]
</dt> <dd>

Tipo: **UINT**

Marcas que controlan esta función. Para ver los valores posibles, *vea el parámetro fuLoad* de la [**función LoadImage.**](/windows/win32/api/winuser/nf-winuser-loadimagea)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **UINT**

Valor distinto de cero si se realiza correctamente; de lo contrario, cero.

## <a name="remarks"></a>Observaciones

**SHExtractIconsW** extrae de los siguientes tipos de archivo.

-   Ejecutable (.exe)
-   DLL (.dll)
-   Icono (.ico)
-   Cursor (.cur)
-   Cursor animado (.ani)
-   Mapa de bits (.bmp)

Extracciones de Windows 3. *También se* admiten archivos ejecutables de 16 bits (.exe o .dll).

Los *parámetros cxIcon* *y cyIcon* especifican el tamaño de los iconos que se extraerán. Se pueden extraer dos tamaños a través de cada parámetro dividiendo el valor entre su LOWORD y HIWORD. Coloque el primer tamaño deseado en el LOWORD del parámetro y el segundo tamaño en HIWORD. Por ejemplo, [**MAKELONG**](/previous-versions/windows/desktop/legacy/ms632660(v=vs.85))(24, 48) para *cxIcon* y *cyIcon* extrae iconos de tamaño 24 y 48.

El proceso de llamada es responsable de destruir todos los iconos extraídos a través de esta función mediante una llamada a la [**función DestroyIcon.**](/windows/win32/api/winuser/nf-winuser-destroyicon)

**SHExtractIconsW** no se exporta por nombre ni se declara en un archivo de encabezado público. Para usarlo, debe declarar un prototipo que coincida y usar [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para solicitar un puntero de función de Shell32.dll que se pueda usar para llamar a esta función.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, solo aplicaciones de escritorio de Windows \[ XP\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                          |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 5.0 o posterior)</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **SHExtractIconsW** (Unicode)<br/>                                                                      |



 

 
