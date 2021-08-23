---
description: El método ReadXMLFile carga un archivo de proyecto XML.
ms.assetid: 8269da74-fb33-42cf-ae8c-fe3d7db27aea
title: Método IXml2Dex::ReadXMLFile (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IXml2Dex.ReadXMLFile
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 37df0c93a17dadc2f6d6fbf94a662b89bf9630a0b0861f5bf5a0c676f7d369fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952444"
---
# <a name="ixml2dexreadxmlfile-method"></a>IXml2Dex::ReadXMLFile (método)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `ReadXMLFile` método carga un archivo de proyecto XML. Este método crea instancias de todos los objetos expresados en el archivo XML y los inserta en la escala de tiempo, así como aplica los atributos dados para la escala de tiempo, como la velocidad de fotogramas o el efecto predeterminado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ReadXMLFile(
   IUnknown *pTimeline,
   BSTR     XMLName
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pTimeline* 
</dt> <dd>

Puntero a la interfaz **IUnknown** de un objeto de escala de tiempo.

</dd> <dt>

*XMLName* 
</dt> <dd>

Cadena que especifica el nombre del archivo que se cargará.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor HRESULT. Estos son algunos de los valores posibles.



| Código devuelto                                                                                                  | Descripción                    |
|--------------------------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                         | Correcto<br/>             |
| <dl> <dt>**FORMATO DE ARCHIVO NO VÁLIDO VFW \_ E \_ \_ \_**</dt> </dl> | Formato de archivo no válido<br/> |



 

## <a name="remarks"></a>Comentarios

Este método no borra los objetos existentes de la escala de tiempo antes de insertar los nuevos objetos definidos en el archivo XML. Si necesita actualizar una escala de tiempo existente, llame primero [**a IAMTimeline::ClearAllGroups.**](iamtimeline-clearallgroups.md)

> [!Note]  
> El archivo de encabezado Qedit.h no es compatible con los encabezados de Direct3D posteriores a la versión 7.

 

> [!Note]  
> Para obtener Qedit.h, descargue la actualización del SDK de [Microsoft Windows para Windows Vista y .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit.h no está disponible en el SDK de Microsoft Windows para Windows 7 y .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Versión<br/> | Internet Explorer 4.0 o posterior<br/>                                               |
| Header<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IXml2Dex (interfaz)**](ixml2dex.md)
</dt> <dt>

[Códigos de error y correcto](error-and-success-codes.md)
</dt> </dl>

 

 




