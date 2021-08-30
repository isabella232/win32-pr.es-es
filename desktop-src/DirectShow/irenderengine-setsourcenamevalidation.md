---
description: El método SetSourceNameValidation especifica cómo el motor de representación valida los nombres de archivo.
ms.assetid: b33904cd-ed7d-41b5-9ebf-50983ec9f7b3
title: Método IRenderEngine::SetSourceNameValidation (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.SetSourceNameValidation
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 7dbf4fadf296b318c74dea19e957c6d33056a81952991aa0cab981674b370313
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120042825"
---
# <a name="irenderenginesetsourcenamevalidation-method"></a>Método IRenderEngine::SetSourceNameValidation

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `SetSourceNameValidation` método especifica cómo el motor de representación valida los nombres de archivo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetSourceNameValidation(
   BSTR          FilterString,
   IMediaLocator *pOverride,
   LONG          Flags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*FilterString* 
</dt> <dd>

**Valor BSTR** que contiene pares de cadenas de filtro, con el formato requerido por el **miembro lpstrFilter** de la [**estructura OPENFILENAME.**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) El localizador de medios usa este filtro si presenta un cuadro de diálogo Abrir archivo al usuario final.

</dd> <dt>

*pOverride* 
</dt> <dd>

Puntero opcional a la [**interfaz IMediaLocator**](imedialocator.md) de un localizador de medios que se usará en lugar del valor predeterminado. Para usar el localizador de medios predeterminado, establezca el valor de este parámetro en **NULL.** Vea Comentarios para obtener más información.

</dd> <dt>

*Marcas* 
</dt> <dd>

Combinación bit a bit de [**marcas de validación de nombre de archivo**](file-name-validation-flags.md) que especifica el comportamiento del localizador de medios. La marca VALIDATEF CHECK de SFN \_ \_ debe estar presente. La marca SFN \_ VALIDATEF \_ hlinkMUTED no tiene ningún efecto con este método.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los siguientes **valores HRESULT:**



| Código devuelto                                                                                            | Descripción                                    |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                   | Correcto.<br/>                            |
| <dl> <dt>**E \_ MUST \_ INIT \_ RENDERER**</dt> </dl> | No se pudo inicializar el motor de representación.<br/> |



 

## <a name="remarks"></a>Comentarios

Con el *parámetro pOverride,* puede proporcionar su propia implementación personalizada de la [**interfaz IMediaLocator.**](imedialocator.md) Por ejemplo, el localizador de medios predeterminado no notifica a una aplicación sobre los archivos que encuentra (o no encuentra). Para evitar esta limitación, podría implementar un localizador de medios personalizado, lo que lo convertiría en un contenedor para la versión predeterminada. A continuación, pase las llamadas [**IMediaLocator::FindMediaFile**](imedialocator-findmediafile.md) directamente a la versión predeterminada y examine el valor devuelto.

Actualmente, este método no valida los orígenes cargados dinámicamente. Vea [**IRenderEngine::SetDynamicReconnectLevel**](irenderengine-setdynamicreconnectlevel.md).

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

[**IRenderEngine (interfaz)**](irenderengine.md)
</dt> <dt>

[Códigos de error y correcto](error-and-success-codes.md)
</dt> </dl>

 

 
