---
description: El método ValidateSourceNames valida los nombres de origen en la escala de tiempo mediante el localizador de medios. Opcionalmente, este método también actualiza cualquier objeto de origen para el que encuentra un archivo.
ms.assetid: 8f4b9ff0-f283-4bcb-83f4-92410cead7db
title: 'IAMTimeline:: ValidateSourceNames (método) (QEDIT. h)'
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
ms.openlocfilehash: 5154926cb9f814c94762b556721c7580e5b0d82c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690615"
---
# <a name="iamtimelinevalidatesourcenames-method"></a>IAMTimeline:: ValidateSourceNames (método)

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `ValidateSourceNames` método valida los nombres de origen en la escala de tiempo mediante el localizador de medios. Opcionalmente, este método también actualiza cualquier objeto de origen para el que encuentra un archivo.

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

Combinación bit a bit de las [**marcas de validación de nombre de archivo**](file-name-validation-flags.md) que especifican el comportamiento del localizador de medios. \_ \_ Deben estar presentes las marcas de comprobación SFN VALIDATEF Replace y SFN \_ VALIDATEF \_ , o bien el método devuelve E \_ INVALIDARG.

</dd> <dt>

*pOverride* 
</dt> <dd>

Puntero opcional a la interfaz [**IMediaLocator**](imedialocator.md) de un localizador de medios que se va a usar en lugar del valor predeterminado. Para usar el localizador de medios predeterminado, establezca el valor de este parámetro en **null**. Vea Comentarios para obtener más información.

</dd> <dt>

*NotifyEventHandle* 
</dt> <dd>

Identificador para un evento. El método señala el evento una vez finalizada la validación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

Con el parámetro *pOverride* , puede proporcionar su propia implementación personalizada de la interfaz [**IMediaLocator**](imedialocator.md) . Por ejemplo, el localizador de medios predeterminado no enviará una notificación a la aplicación sobre los archivos que encuentre (o no puede encontrar). Para superar esta limitación, puede implementar un localizador de medios personalizado, convirtiéndolo en un contenedor para la versión predeterminada. En la versión personalizada, pase [**IMediaLocator:: FindMediaFile**](imedialocator-findmediafile.md) llamadas directamente a la versión predeterminada y examine el valor devuelto.

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

[**Interfaz IAMTimeline**](iamtimeline.md)
</dt> <dt>

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> </dl>

 

 




