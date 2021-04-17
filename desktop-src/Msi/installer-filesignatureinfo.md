---
description: El método FileSignatureInfo del objeto Installer toma la ruta de acceso a un archivo y devuelve una matriz SAFEARRAY de bytes que representan el hash o el certificado codificado.
ms.assetid: ab34bc46-8a8f-4b48-a1d1-d824ff36a9cc
title: Instalador. FileSignatureInfo (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.FileSignatureInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 5dbb758118b7612aaef3f7cca744674bca1c768d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653335"
---
# <a name="installerfilesignatureinfo-method"></a>Instalador. FileSignatureInfo (método)

El método **FileSignatureInfo** del objeto [**Installer**](installer-object.md) toma la ruta de acceso a un archivo y devuelve una matriz SafeArray de bytes que representan el hash o el certificado codificado. Los valores se pueden usar para rellenar las tablas [MsiDigitalSignature](msidigitalsignature-table.md), [MsiPatchCertificate](msipatchcertificate-table.md)y [MsiDigitalCertificate](msidigitalcertificate-table.md) .

Para obtener más información, vea el [**tipo de datos SafeArray**](/windows/win32/api/oaidl/ns-oaidl-safearray).

## <a name="syntax"></a>Sintaxis


```JScript
Installer.FileSignatureInfo(
  FilePath,
  Options,
  Format
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*FilePath* 
</dt> <dd>

Ruta de acceso completa a un archivo firmado digitalmente.

Al rellenar las tablas [MsiDigitalSignature](msidigitalsignature-table.md) y [MsiDigitalCertificate](msidigitalcertificate-table.md) , *filePath* apunta a un archivo. CAB firmado digitalmente. Al rellenar las tablas [MsiPatchCertificate](msipatchcertificate-table.md) y MsiDigitalCertificate, *filePath* apunta a una revisión firmada digitalmente.

</dd> <dt>

*Opciones* 
</dt> <dd>

Marcas de caso de error especiales.



| Marca                                                                                                                                                                                                                                                                                                                                    | Significado                                                                                                                                                                                                                                                                                                                                        |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiSignatureOptionInvalidHashFatal"></span><span id="msisignatureoptioninvalidhashfatal"></span><span id="MSISIGNATUREOPTIONINVALIDHASHFATAL"></span><dl> <dt>**msiSignatureOptionInvalidHashFatal**</dt> <dt>1</dt> </dl> | Con *Options* establecido en MsiSignatureOptionInvalidHashFatal, **FileSignatureInfo** siempre devuelve un error irrecuperable para un hash no válido. <br/> Si *Options* no se establece en MsiSignatureOptionInvalidHashFatal y *Format* se establece en msiSignatureInfoCertificate, **FileSignatureInfo** no devuelve un error para un hash no válido.<br/> |



 

</dd> <dt>

*Format* 
</dt> <dd>

Información de firma solicitada.



| Marca                                                                                                                                                                                                                                                                                                        | Significado                                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span id="msiSignatureInfoCertificate"></span><span id="msisignatureinfocertificate"></span><span id="MSISIGNATUREINFOCERTIFICATE"></span><dl> <dt>**msiSignatureInfoCertificate**</dt> <dt>0</dt> </dl> | Devuelve una matriz SAFEARRAY de bytes que representan el certificado codificado.<br/> |
| <span id="msiSignatureInfoHash"></span><span id="msisignatureinfohash"></span><span id="MSISIGNATUREINFOHASH"></span><dl> <dt>**msiSignatureInfoHash**</dt> <dt>1</dt> </dl>                             | Devuelve una matriz SAFEARRAY de bytes que representa el hash.<br/>                |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si es correcto, el método devuelve una [matriz SafeArray](/windows/win32/api/oaidl/ns-oaidl-safearray) de bytes que contienen el hash o el certificado codificado.

## <a name="remarks"></a>Observaciones

Para crear una instalación firmada completamente comprobada mediante la automatización, use el método **FileSignatureInfo** para rellenar las tablas [MsiDigitalCertificate](msidigitalcertificate-table.md), [MsiPatchCertificate](msipatchcertificate-table.md)y [MsiDigitalSignature](msidigitalsignature-table.md) . Para obtener más información, vea [crear una instalación firmada completamente comprobada mediante automatización](authoring-a-fully-verified-signed-installation-using-automation.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller se define como 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Crear una instalación firmada completamente comprobada mediante automatización](authoring-a-fully-verified-signed-installation-using-automation.md)
</dt> <dt>

[Firmas digitales y Windows Installer](digital-signatures-and-windows-installer.md)
</dt> <dt>

[**MsiGetFileSignatureInformation**](/windows/desktop/api/Msi/nf-msi-msigetfilesignatureinformationa)
</dt> </dl>

 

 
