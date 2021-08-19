---
description: El método FindMediaFile busca un archivo y, si se realiza correctamente, recupera la ruta de acceso al archivo.
ms.assetid: ddfa2c75-e51f-4aad-afe6-8a60c46e8d35
title: Método IMediaLocator::FindMediaFile (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaLocator.FindMediaFile
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: cc1acda4a3bc6e2d93ae8b7024ef34f759c11c5c4d487a09d3be3a3542e0c445
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117818942"
---
# <a name="imedialocatorfindmediafile-method"></a>IMediaLocator::FindMediaFile (método)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El método busca un archivo y, si se realiza `FindMediaFile` correctamente, recupera la ruta de acceso al archivo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT FindMediaFile(
   BSTR Input,
   BSTR FilterString,
   BSTR *pOutput,
   long Flags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Entrada* 
</dt> <dd>

Nombre de archivo, incluida la ruta de acceso, donde se sabe que reside por última vez el archivo. Para los objetos de origen de la escala de tiempo, use el nombre del medio actual.

</dd> <dt>

*FilterString* 
</dt> <dd>

BSTR **que** contiene pares de cadenas de filtro, con el formato requerido por el miembro **lpstrFilter** de la [**estructura OPENFILENAME.**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) El localizador de medios usa este filtro si muestra un cuadro de diálogo Abrir archivo. El valor puede ser **NULL si** el *parámetro Flags* no incluye la marca \_ POPUP VALIDATEF de SFN. \_

</dd> <dt>

*pOutput* 
</dt> <dd>

Puntero a una variable que recibe la ruta de acceso real al  archivo, si difiere del valor contenido en Entrada y si el método encuentra correctamente el archivo.

</dd> <dt>

*Marcas* 
</dt> <dd>

Combinación bit a bit de cero o más marcas. Para obtener una lista de las marcas posibles, vea [**Marcas de validación de nombres de archivo**](file-name-validation-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Comentarios

La cadena de filtro del cuadro de diálogo Abrir archivo, especificada por el *parámetro FilterString,* contiene caracteres NULL internos. Por ejemplo, Video \\ 0 \*.avi\\ 0 \\ 0 es una cadena de filtro válida. No se puede usar la función **SysAllocStr** para asignar el BSTR, porque esa función espera una cadena terminada en NULL y truncará la cadena en el primer carácter NULL. Por lo tanto, use una función como **SysAllocStringLen**, que incluye un parámetro explícito para la longitud:


```C++
BSTR filter = SysAllocStringLen(L"Video\0*.avi\0", 12);
// Note: SysAllocStringLen appends an additional '\0' to the string.
```



Si el usuario cancela el cuadro de diálogo Abrir archivo, el método devuelve E \_ FAIL.

El método asigna memoria para **el BSTR** en *pOutput*. La aplicación debe llamar **a SysFreeString para** liberar la memoria.

> [!Note]  
> El archivo de encabezado Qedit.h no es compatible con los encabezados de Direct3D posteriores a la versión 7.

 

> [!Note]  
> Para obtener Qedit.h, descargue la actualización del SDK de [Microsoft Windows para Windows Vista y .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit.h no está disponible en el SDK de Microsoft Windows para Windows 7 y .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMediaLocator (interfaz)**](imedialocator.md)
</dt> <dt>

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> </dl>

 

 
