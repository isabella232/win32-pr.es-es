---
description: El método ValidateSourceNames valida los nombres de origen en la escala de tiempo, mediante el localizador de medios. Opcionalmente, este método también actualiza cualquier objeto de origen para el que busque un archivo.
ms.assetid: 8f4b9ff0-f283-4bcb-83f4-92410cead7db
title: Método IAMTimeline::ValidateSourceNames (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.ValidateSourceNames
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: cabaa5f9ec67abaf8805ad55917d0a33b6ad3457bedd8899b3f443f1a247b8d6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120043115"
---
# <a name="iamtimelinevalidatesourcenames-method"></a>IamTimeline::ValidateSourceNames (método)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `ValidateSourceNames` método valida los nombres de origen en la escala de tiempo, mediante el localizador de medios. Opcionalmente, este método también actualiza cualquier objeto de origen para el que busque un archivo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ValidateSourceNames(
   long          ValidateFlags,
   IMediaLocator *pOverride,
   long          NotifyEventHandle
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ValidateFlags* 
</dt> <dd>

Combinación bit a bit de [**marcas de validación de nombre de archivo**](file-name-validation-flags.md) que especifica el comportamiento del localizador de medios. Las marcas SFN VALIDATEF REPLACE y SFN VALIDATEF CHECK deben estar presentes, o bien el método \_ \_ devuelve E \_ \_ \_ INVALIDARG.

</dd> <dt>

*pOverride* 
</dt> <dd>

Puntero opcional a la [**interfaz IMediaLocator**](imedialocator.md) de un localizador de medios que se usará en lugar del valor predeterminado. Para usar el localizador de medios predeterminado, establezca el valor de este parámetro en **NULL.** Vea Comentarios para obtener más información.

</dd> <dt>

*NotifyEventHandle* 
</dt> <dd>

Identificador para un evento. El método señala el evento después de haber completado la validación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Comentarios

Con el *parámetro pOverride,* puede proporcionar su propia implementación personalizada de la [**interfaz IMediaLocator.**](imedialocator.md) Por ejemplo, el localizador de medios predeterminado no notificará a la aplicación sobre los archivos que encuentra (o no puede encontrar). Para evitar esta limitación, podría implementar un localizador de medios personalizado, lo que lo convertiría en un contenedor para la versión predeterminada. En la versión personalizada, pase [**las llamadas IMediaLocator::FindMediaFile**](imedialocator-findmediafile.md) directamente a la versión predeterminada y examine el valor devuelto.

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

[**IAMTimeline (interfaz)**](iamtimeline.md)
</dt> <dt>

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> </dl>

 

 




