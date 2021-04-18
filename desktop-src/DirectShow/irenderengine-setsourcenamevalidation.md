---
description: El método SetSourceNameValidation especifica cómo valida el motor de representación los nombres de archivo.
ms.assetid: b33904cd-ed7d-41b5-9ebf-50983ec9f7b3
title: 'IRenderEngine:: SetSourceNameValidation (método) (QEDIT. h)'
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
ms.openlocfilehash: 96164a817fd04f505b32c17be1bff3268e847df8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680709"
---
# <a name="irenderenginesetsourcenamevalidation-method"></a>IRenderEngine:: SetSourceNameValidation (método)

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `SetSourceNameValidation` método especifica cómo valida el motor de representación los nombres de archivo.

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

Valor **BSTR** que contiene pares de cadenas de filtro, con el formato que requiere el miembro **lpstrFilter** de la estructura [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) . El localizador de medios usa este filtro si presenta un cuadro de diálogo Abrir archivo al usuario final.

</dd> <dt>

*pOverride* 
</dt> <dd>

Puntero opcional a la interfaz [**IMediaLocator**](imedialocator.md) de un localizador de medios que se va a usar en lugar del valor predeterminado. Para usar el localizador de medios predeterminado, establezca el valor de este parámetro en **null**. Vea Comentarios para obtener más información.

</dd> <dt>

*Marcas* 
</dt> <dd>

Combinación bit a bit de las [**marcas de validación de nombre de archivo**](file-name-validation-flags.md) que especifican el comportamiento del localizador de medios. La marca de comprobación de SFN \_ VALIDATEF \_ debe estar presente. La \_ \_ marca HLINKMUTED VALIDATEF SFN no tiene ningún efecto en este método.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los siguientes valores **HRESULT** :



| Código devuelto                                                                                            | Descripción                                    |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>                   | Correcto.<br/>                            |
| <dl> <dt>**E \_ debe \_ inicializar el \_ representador**</dt> </dl> | No se pudo inicializar el motor de representación.<br/> |



 

## <a name="remarks"></a>Observaciones

Con el parámetro *pOverride* , puede proporcionar su propia implementación personalizada de la interfaz [**IMediaLocator**](imedialocator.md) . Por ejemplo, el localizador de medios predeterminado no notifica a una aplicación los archivos que encuentra (o no puede encontrar). Para superar esta limitación, puede implementar un localizador de medios personalizado, convirtiéndolo en un contenedor para la versión predeterminada. Después, pase las llamadas a [**IMediaLocator:: FindMediaFile**](imedialocator-findmediafile.md) directamente a la versión predeterminada y examine el valor devuelto.

Actualmente, este método no valida los orígenes cargados dinámicamente. Vea [**IRenderEngine:: SetDynamicReconnectLevel**](irenderengine-setdynamicreconnectlevel.md).

> [!Note]  
> El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.

 

> [!Note]  
> Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>QEDIT. h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IRenderEngine**](irenderengine.md)
</dt> <dt>

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> </dl>

 

 
