---
description: El método ReadXMLFile carga un archivo de proyecto XML.
ms.assetid: 8269da74-fb33-42cf-ae8c-fe3d7db27aea
title: 'IXml2Dex:: ReadXMLFile (método) (QEDIT. h)'
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
ms.openlocfilehash: 5b0fb5104e56afbcc4dd25e28981f0c382d7888e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690916"
---
# <a name="ixml2dexreadxmlfile-method"></a>IXml2Dex:: ReadXMLFile (método)

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `ReadXMLFile` método carga un archivo de proyecto XML. Este método crea instancias de todos los objetos expresados en el archivo XML y los inserta en la escala de tiempo, así como la aplicación de los atributos proporcionados para la escala de tiempo, como la velocidad de fotogramas o el efecto predeterminado.

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

Puntero a la interfaz **IUnknown** de un objeto Timeline.

</dd> <dt>

*XMLName* 
</dt> <dd>

Cadena que especifica el nombre del archivo que se va a cargar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor HRESULT. Estos son algunos de los valores posibles.



| Código devuelto                                                                                                  | Descripción                    |
|--------------------------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>                         | Correcto<br/>             |
| <dl> <dt>**\_formato de \_ archivo no válido de VFW E \_ \_**</dt> </dl> | Formato de archivo no válido<br/> |



 

## <a name="remarks"></a>Observaciones

Este método no borra los objetos existentes de la escala de tiempo antes de insertar los nuevos objetos definidos en el archivo XML. Si necesita actualizar una escala de tiempo existente, llame a [**IAMTimeline:: ClearAllGroups**](iamtimeline-clearallgroups.md) en primer lugar.

> [!Note]  
> El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.

 

> [!Note]  
> Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Versión<br/> | Internet Explorer 4,0 o posterior<br/>                                               |
| Encabezado<br/>  | <dl> <dt>QEDIT. h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IXml2Dex**](ixml2dex.md)
</dt> <dt>

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> </dl>

 

 




