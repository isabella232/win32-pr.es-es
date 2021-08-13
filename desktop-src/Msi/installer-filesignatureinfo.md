---
description: El método FileSignatureInfo del objeto Installer toma la ruta de acceso a un archivo y devuelve una SAFEARRAY de bytes que representan el hash o el certificado codificado.
ms.assetid: ab34bc46-8a8f-4b48-a1d1-d824ff36a9cc
title: Método Installer.FileSignatureInfo
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
ms.openlocfilehash: 670b5ba6deb4a53429180e832c2a49e4968c53efbe7c54cdf50e62e20bf5503b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118630786"
---
# <a name="installerfilesignatureinfo-method"></a>Método Installer.FileSignatureInfo

El **método FileSignatureInfo** del objeto [**Installer**](installer-object.md) toma la ruta de acceso a un archivo y devuelve una SAFEARRAY de bytes que representan el hash o el certificado codificado. Los valores se pueden usar para rellenar las tablas [MsiDigitalSignature,](msidigitalsignature-table.md) [MsiPatchCertificate](msipatchcertificate-table.md)y [MsiDigitalCertificate.](msidigitalcertificate-table.md)

Para obtener más información, vea el [**tipo de datos SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray).

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

Al rellenar las tablas [MsiDigitalSignature](msidigitalsignature-table.md) y [MsiDigitalCertificate,](msidigitalcertificate-table.md) *FilePath* apunta a un contenedor firmado digitalmente. Al rellenar las tablas [MsiPatchCertificate](msipatchcertificate-table.md) y MsiDigitalCertificate, *FilePath* apunta a una revisión firmada digitalmente.

</dd> <dt>

*Opciones* 
</dt> <dd>

Marcas de casos de error especiales.



| Marca                                                                                                                                                                                                                                                                                                                                    | Significado                                                                                                                                                                                                                                                                                                                                        |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiSignatureOptionInvalidHashFatal"></span><span id="msisignatureoptioninvalidhashfatal"></span><span id="MSISIGNATUREOPTIONINVALIDHASHFATAL"></span><dl> <dt>**msiSignatureOptionInvalidHashFatal**</dt> <dt>1</dt> </dl> | Con *Opciones* establecido en msiSignatureOptionInvalidHashFatal, **FileSignatureInfo** siempre devuelve un error irrespeto para un hash no válido. <br/> Si *Options* no está establecido en msiSignatureOptionInvalidHashFatal y *Format* está establecido en msiSignatureInfoCertificate, **FileSignatureInfo** no devuelve un error para un hash no válido.<br/> |



 

</dd> <dt>

*Format* 
</dt> <dd>

Información de firma solicitada.



| Marca                                                                                                                                                                                                                                                                                                        | Significado                                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span id="msiSignatureInfoCertificate"></span><span id="msisignatureinfocertificate"></span><span id="MSISIGNATUREINFOCERTIFICATE"></span><dl> <dt>**msiSignatureInfoCertificate**</dt> <dt>0</dt> </dl> | Devuelve una SAFEARRAY de bytes que representan el certificado codificado.<br/> |
| <span id="msiSignatureInfoHash"></span><span id="msisignatureinfohash"></span><span id="MSISIGNATUREINFOHASH"></span><dl> <dt>**msiSignatureInfoHash**</dt> <dt>1</dt> </dl>                             | Devuelve una SAFEARRAY de bytes que representan el hash.<br/>                |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si se realiza correctamente, el método devuelve [una SAFEARRAY](/windows/win32/api/oaidl/ns-oaidl-safearray) de bytes que contienen el hash o el certificado codificado.

## <a name="remarks"></a>Observaciones

Para crear una instalación firmada totalmente verificada mediante automatización, use el método **FileSignatureInfo** para rellenar las tablas [MsiDigitalCertificate,](msidigitalcertificate-table.md) [MsiPatchCertificate](msipatchcertificate-table.md)y [MsiDigitalSignature.](msidigitalsignature-table.md) Para obtener más información, [vea Creación de una instalación firmada totalmente comprobada mediante Automation.](authoring-a-fully-verified-signed-installation-using-automation.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IInstaller de IID se define como \_ 000C1090-0000-0000-C000-00000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Creación de una instalación firmada totalmente verificada mediante Automation](authoring-a-fully-verified-signed-installation-using-automation.md)
</dt> <dt>

[Instalador de firmas digitales Windows datos](digital-signatures-and-windows-installer.md)
</dt> <dt>

[**MsiGetFileSignatureInformation**](/windows/desktop/api/Msi/nf-msi-msigetfilesignatureinformationa)
</dt> </dl>

 

 
