---
description: El método Directory recupera una lista de archivos del tipo especificado del directorio actual.
ms.assetid: 0ae89811-7534-497b-af9f-ae37a48bc3e5
title: ISCardFileAccess::D irectory (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.Directory
api_type:
- COM
api_location: ''
ms.openlocfilehash: 009263a92f014367636c7ff16b7f43635f73fa1b2ed17b52d53e81152c6e15b6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119481305"
---
# <a name="iscardfileaccessdirectory-method"></a>ISCardFileAccess::D irectory (método)

\[El **método Directory** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]

El **método Directory** recupera una lista de archivos del tipo especificado del directorio actual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Directory(
  [in]  FILETYPE    fileType,
  [out] LPSAFEARRAY *ppFileList
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*fileType* \[ En\]
</dt> <dd>

Tipo de [*archivos de tarjeta inteligente*](../secgloss/s-gly.md) que se va a enumerar.



| Value                                                                                                                                                                                      | Significado                                              |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <span id="SC_TYPE_DIRECTORIES"></span><span id="sc_type_directories"></span><dl> <dt>**DIRECTORIOS \_ DE TIPO \_ SC**</dt> </dl>           | Enumerar solo archivos de directorio.<br/>                |
| <span id="SC_TYPE_FILES"></span><span id="sc_type_files"></span><dl> <dt>**ARCHIVOS \_ DE TIPO \_ SC**</dt> </dl>                             | Enumerar solo archivos elementales.<br/>               |
| <span id="SC_TYPE_ALL_FILES"></span><span id="sc_type_all_files"></span><dl> <dt>**SC \_ ESCRIBA TODOS LOS \_ \_ ARCHIVOS**</dt> </dl>                | Enumera los archivos de directorio y elementales.<br/> |
| <span id="SC_TYPE_DIRECTORY_FILE"></span><span id="sc_type_directory_file"></span><dl> <dt>**ARCHIVO \_ DE DIRECTORIO DE TIPO \_ \_ SC**</dt> </dl> | Archivo de directorio.<br/>                           |
| <span id="SC_TYPE_TRANSPARENT_EF"></span><span id="sc_type_transparent_ef"></span><dl> <dt>**EF \_ \_ TRANSPARENTE DE TIPO \_ SC**</dt> </dl> | Archivo elemental transparente.<br/>              |
| <span id="SC_TYPE_FIXED_EF"></span><span id="sc_type_fixed_ef"></span><dl> <dt>**EF \_ \_ FIJO DE TIPO \_ SC**</dt> </dl>                   | Archivo elemental fijo lineal.<br/>             |
| <span id="SC_TYPE_CYCLIC_EF"></span><span id="sc_type_cyclic_ef"></span><dl> <dt>**SC \_ TYPE \_ CYCLIC \_ EF**</dt> </dl>                | Archivo elemental cíclico.<br/>                   |
| <span id="SC_TYPE_VARIABLE_EF"></span><span id="sc_type_variable_ef"></span><dl> <dt>**VARIABLE \_ DE TIPO SC \_ \_ EF**</dt> </dl>          | Archivo elemental de variable lineal.<br/>          |



 

</dd> <dt>

*ppFileList* \[ out\]
</dt> <dd>

Matriz de BSTR que representa la lista de archivos que coinciden con el especificador en *fileType*.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve uno de los siguientes valores posibles.



| Código devuelto                                                                                   | Descripción                                               |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | La operación se completó correctamente.<br/>          |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Parámetro no válido.<br/>                             |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | La interfaz no ha implementado este método.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insuficiente<br/>                                 |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl>     | Se pasó un puntero no válido para *ppFileList.*<br/>  |



 

## <a name="remarks"></a>Observaciones

Para obtener una lista de todos los métodos definidos por esta interfaz, vea [**ISCardFileAccess.**](iscardfileaccess.md)

Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de tarjeta inteligente si se llamó a una función de tarjeta inteligente para completar la solicitud. Para obtener más información, vea [Valores devueltos de tarjeta inteligente.](authentication-return-values.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/> |
| Fin de compatibilidad de cliente<br/>    | Windows XP<br/>                                |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                       |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ISCardFileAccess**](iscardfileaccess.md)
</dt> </dl>

 

 
