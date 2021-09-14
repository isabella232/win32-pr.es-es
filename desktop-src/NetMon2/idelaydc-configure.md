---
description: El método Configure envía la información de configuración utilizada para una captura.
ms.assetid: 6418c465-c339-44b6-84eb-36c7b89231f8
title: Método IDelaydCConfigure (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.Configure
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 0fa91c5b46d2eb7ca21ba14aa00b274d52e77eb1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074142"
---
# <a name="idelaydcconfigure-method"></a>IDelaydC::Configure (método)

El **método Configure** envía la información de configuración utilizada para una captura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT STDMETHODCALLTYPE Configure(
  [in]  HBLOB hConfigurationBlob,
  [out] HBLOB hErrorBlob
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hConfigurationBlob* \[ En\]
</dt> <dd>

Controle el BLOB que contiene la información de configuración.

</dd> <dt>

*hErrorBlob* \[ out\]
</dt> <dd>

Controlar un blob de error que contiene información de error adicional. Para obtener información sobre el contenido de un BLOB de error, vea la sección Comentarios de este tema .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, el valor devuelto es NMERR \_ SUCCESS.

Si el método no se realiza correctamente, el valor devuelto es uno de los siguientes códigos de error:



| Código devuelto                                                                                                      | Descripción                                                                               |
|------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <dl> <dt>**CAPTURA DE \_ NMERR**</dt> </dl>                  | El NPP informa de que se ha iniciado la sesión de captura.<br/>                          |
| <dl> <dt>**DISCO NMERR \_ \_ NO FIJO \_ \_ LOCAL**</dt> </dl>    |                                                                                           |
| <dl> <dt>**NMERR \_ NO PUDO CREAR \_ \_ \_ MEMORIA**</dt> </dl> |                                                                                           |
| <dl> <dt>**MEMORIA DE NMERR \_ \_ FUERA DE LA \_ MEMORIA**</dt> </dl>            | No había memoria disponible. Apague las ventanas para liberar recursos.<br/>               |
| <dl> <dt>**NMERR \_ INVALID \_ PARAMETER**</dt> </dl>         | El BLOB de configuración especificado por el parámetro hConfiguration no es válido.<br/> |



 

## <a name="remarks"></a>Observaciones

Debe aplicar este método para reiniciar un NPP que se ha iniciado, detenido, pero no desconectado.

El blob de error devuelto por *hErrorBlob* contiene entradas que Monitor de red no se pudieron entender ni encontrar en el BLOB de configuración especificado en *hConfigurationBlob*. El BLOB de error devuelto contiene información de error que la aplicación puede usar para solucionar problemas. Por ejemplo, si se devuelve NMERR BLOB ENTRY DOES NOT EXIST, la entrada Monitor de red no se encuentra se incluye en el \_ \_ blob de error \_ \_ \_ devuelto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                                                                     |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| Archivo DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[IDelaydC](idelaydc.md)
</dt> <dt>

[IDelaydC::Conectar](idelaydc-connect.md)
</dt> <dt>

[IDelaydC::Start](idelaydc-start.md)
</dt> <dt>

[IDelaydC::Stop](idelaydc-stop.md)
</dt> </dl>

 

 




