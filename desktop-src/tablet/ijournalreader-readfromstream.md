---
description: Toma un flujo a un archivo de notas de Journal y devuelve una secuencia XML que representa el contenido del documento.
ms.assetid: 5a169dfe-b102-4aef-9efe-5db2cd2fb96f
title: 'IJournalReader:: ReadFromStream (método) (Journal. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IJournalReader.ReadFromStream
api_type:
- COM
api_location:
- Journal.dll
ms.openlocfilehash: 258ac30b8857fa4ef24bd86a08c7e402229f4bff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696250"
---
# <a name="ijournalreaderreadfromstream-method"></a>IJournalReader:: ReadFromStream (método)

Toma un flujo a un archivo de notas de Journal y devuelve una secuencia XML que representa el contenido del documento.

> [!Note]  
> El componente lector del diario no puede leer archivos de Windows Journal creados por equipos que ejecutan Windows 7 o posterior. La interfaz IJournalReader se debe considerar en desuso u obsoleta y no debe usarse.

 

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ReadFromStream(
  [in]          IStream *pJournalFileStream,
  [out, retval] IStream **ppXmlStream
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pJournalFileStream* \[ de\]
</dt> <dd>

Objeto [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) que representa el archivo de diario que se va a leer.

</dd> <dt>

*ppXmlStream* \[ out, retval\]
</dt> <dd>

Un puntero a la dirección de un objeto [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) que recibirá el flujo XML creado mediante la lectura del archivo de diario.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

Las secuencias se utilizan para evitar el acceso directo al sistema de archivos y para permitir la elección del método de análisis de XML que se va a usar.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente de un controlador del evento [**click**](/dotnet/api/system.windows.forms.control.click?view=netcore-3.1) de un botón se crea una instancia de la interfaz de la [**interfaz IJournalReader**](ijournalreader.md) y se usa para leer un archivo de diario existente.


```C++
void CJntlReaderMFCDlg::OnBnClickedButton1()
{
  IStream* pJntStream;
  IStream* pXmlStream;
  IJournalReader* pJntReader;
  HRESULT hr;
  CString szFileName = "";
  static char BASED_CODE szFilter[] = 
    "Journal files (*.jnt)|*.jnt|All files (*.*)|*.*";
  CFileDialog* fileDialog = new CFileDialog(TRUE, "*.jnt", NULL, 
                                 OFN_FILEMUSTEXIST, szFilter, this);

  // Get the filename from the user by using a File Open dialog
  if (IDOK == fileDialog->DoModal())
  {
    szFileName = fileDialog->GetPathName();

    // Read a JNT file into a memory buffer
    HANDLE hFile = CreateFile(szFileName.GetBuffer(), GENERIC_READ, FILE_SHARE_READ, NULL, OPEN_EXISTING, FILE_ATTRIBUTE_NORMAL, NULL);
    
    if (INVALID_HANDLE_VALUE != hFile)
    {
      // Allocate memory to hold the file contents
      DWORD dwFileSize = GetFileSize(hFile, NULL);
      HGLOBAL hGlobal = GlobalAlloc(GHND, dwFileSize);

      if (hGlobal != NULL)
      {
        LPBYTE pData = (LPBYTE)GlobalLock(hGlobal);

        if (pData != NULL)
        {
          DWORD dwRead;

          // Read the Journal file into the pData buffer
          if (ReadFile(hFile, pData, dwFileSize, &dwRead, NULL) && dwRead == dwFileSize)
          {
            // Create an IStream that points to the buffer
            hr = CreateStreamOnHGlobal(hGlobal, FALSE, &pJntStream);

            if (SUCCEEDED(hr))
            {
              // Create a JournalReader object
              hr = CoCreateInstance(CLSID_JournalReader, NULL, CLSCTX_ALL, 
                          IID_IJournalReader, (void**)&pJntReader);

              if (SUCCEEDED(hr))
              {
                // Read in the JNT file by using the JournalReader
                hr = pJntReader->ReadFromStream(pJntStream, &pXmlStream);

                // Display results
                if (SUCCEEDED(hr))
                {
                  DisplayXml(pXmlStream);
                }

                // Clean up
                pXmlStream->Release();
                pJntReader = NULL;
                pJntStream->Release();
              }
            }
          }
          GlobalUnlock(hGlobal);
        }
        GlobalFree(hGlobal);
      }
    }
  }
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                                                     |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                         |
| Encabezado<br/>                   | <dl> <dt>Journal. h (también requiere Journal \_ i. c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Journal.dll</dt> </dl>                            |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IJournalReader**](ijournalreader.md)
</dt> <dt>

[Referencia del esquema del lector de Journal](journal-reader-schema-reference.md)
</dt> </dl>

 

