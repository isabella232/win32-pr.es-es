---
description: Proporciona acceso al contexto de un objeto de almacén de CAPICOM. Este contexto permite usar el almacén de certificados de CAPICOM en otras derivaciones de CryptoAPI.
ms.assetid: dc108e2d-d6ec-4972-9c8e-e6e738c25756
title: Interfaz ICertStore
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ICertStore
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 119609399709340049bc43693ac51f6259021416
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690475"
---
# <a name="icertstore-interface"></a>Interfaz ICertStore

\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.\]

La interfaz **ICertStore** proporciona acceso al contexto de un objeto de [**almacén**](store.md) de CAPICOM. Este contexto permite usar el almacén de certificados de CAPICOM en otras derivaciones de CryptoAPI.

## <a name="when-to-use"></a>Cuándo se usa

Use esta interfaz cuando necesite usar un objeto de [**almacén**](store.md) de CAPICOM en otra derivación de CryptoAPI.

## <a name="members"></a>Miembros

La interfaz **ICertStore** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La interfaz **ICertStore** tiene estos métodos.



| Método                                        | Descripción                                                                                                         |
|:----------------------------------------------|:--------------------------------------------------------------------------------------------------------------------|
| [**CloseHandle**](icertstore-closehandle.md) | Cierra un identificador HCERTSTORE adquirido a través de la propiedad [**StoreHandle**](icertstore-storehandle.md) .<br/> |



 

### <a name="properties"></a>Propiedades

La interfaz **ICertStore** tiene estas propiedades.



| Propiedad                                                     | Tipo de acceso           | Descripción                                                                                                         |
|:-------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------|
| [**StoreHandle**](icertstore-storehandle.md)<br/>     | Lectura/escritura<br/> | Establece o recupera el identificador HCERTSTORE de un almacén de certificados.<br/>                                          |
| [**StoreLocation**](icertstore-storelocation.md)<br/> | Lectura/escritura<br/> | Establece o recupera la [**Ubicación del \_ almacén \_ de CAPICOM**](capicom-store-location.md) de un almacén de certificados.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 




